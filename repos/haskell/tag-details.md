<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `haskell`

-	[`haskell:8`](#haskell8)
-	[`haskell:8-buster`](#haskell8-buster)
-	[`haskell:8-slim`](#haskell8-slim)
-	[`haskell:8-slim-buster`](#haskell8-slim-buster)
-	[`haskell:8.10`](#haskell810)
-	[`haskell:8.10-buster`](#haskell810-buster)
-	[`haskell:8.10-slim`](#haskell810-slim)
-	[`haskell:8.10-slim-buster`](#haskell810-slim-buster)
-	[`haskell:8.10.7`](#haskell8107)
-	[`haskell:8.10.7-buster`](#haskell8107-buster)
-	[`haskell:8.10.7-slim`](#haskell8107-slim)
-	[`haskell:8.10.7-slim-buster`](#haskell8107-slim-buster)
-	[`haskell:9`](#haskell9)
-	[`haskell:9-buster`](#haskell9-buster)
-	[`haskell:9-slim`](#haskell9-slim)
-	[`haskell:9-slim-buster`](#haskell9-slim-buster)
-	[`haskell:9.0`](#haskell90)
-	[`haskell:9.0-buster`](#haskell90-buster)
-	[`haskell:9.0-slim`](#haskell90-slim)
-	[`haskell:9.0-slim-buster`](#haskell90-slim-buster)
-	[`haskell:9.0.2`](#haskell902)
-	[`haskell:9.0.2-buster`](#haskell902-buster)
-	[`haskell:9.0.2-slim`](#haskell902-slim)
-	[`haskell:9.0.2-slim-buster`](#haskell902-slim-buster)
-	[`haskell:9.2`](#haskell92)
-	[`haskell:9.2-buster`](#haskell92-buster)
-	[`haskell:9.2-slim`](#haskell92-slim)
-	[`haskell:9.2-slim-buster`](#haskell92-slim-buster)
-	[`haskell:9.2.2`](#haskell922)
-	[`haskell:9.2.2-buster`](#haskell922-buster)
-	[`haskell:9.2.2-slim`](#haskell922-slim)
-	[`haskell:9.2.2-slim-buster`](#haskell922-slim-buster)
-	[`haskell:buster`](#haskellbuster)
-	[`haskell:latest`](#haskelllatest)
-	[`haskell:slim`](#haskellslim)
-	[`haskell:slim-buster`](#haskellslim-buster)

## `haskell:8`

```console
$ docker pull haskell@sha256:aaa408ad7e7eff6cd76c39feae223db7ba3550b937e833e78958478334fc9afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:8` - linux; amd64

```console
$ docker pull haskell@sha256:c70ba511d11de63ebcfb93e74b0da327ee9893ef933c87d4514c405d4e087f75
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.5 MB (529538103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7654255acc2e886b1340b582489f7732497d7ce8396edb54b721cd3e0d0dcb`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:37 GMT
ADD file:7c5789fb822bda2652d7addee832c5a3d71733f0f94f97d89b0c5570c0840829 in / 
# Wed, 20 Apr 2022 04:43:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:28:53 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:29:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:29:16 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:29:17 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:29:19 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:32:24 GMT
ARG LLVM_VERSION=12
# Wed, 20 Apr 2022 09:32:24 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 20 Apr 2022 09:32:25 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 20 Apr 2022 09:34:56 GMT
ARG GHC=8.10.7
# Wed, 20 Apr 2022 09:34:56 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 20 Apr 2022 09:35:57 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:36:04 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:36:04 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:36:08 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:36:08 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:36:08 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:85bed84afb9a834cf090b55d2e584abd55b4792d93b750db896f486680638344`  
		Last Modified: Wed, 20 Apr 2022 04:48:49 GMT  
		Size: 50.4 MB (50436985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b522b8c18adf55149c7dd6ddd4becc626f002e805952405cc9904c55e038c4c2`  
		Last Modified: Wed, 20 Apr 2022 09:38:19 GMT  
		Size: 120.6 MB (120639968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bbb5b2ebcc192a387282f0d58027a5e65da5844d39689ac323a0d7192d6e7a`  
		Last Modified: Wed, 20 Apr 2022 09:38:02 GMT  
		Size: 10.0 MB (10032282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4cf90ffbaa9b2eb22b002bc5540ca94e5f7f0382bf6797baf23095f63f7fab`  
		Last Modified: Wed, 20 Apr 2022 09:44:16 GMT  
		Size: 330.5 MB (330502214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0434fc716c3d7af8358295c79b97e856e8effd26893a9abc59eccca76d68f2`  
		Last Modified: Wed, 20 Apr 2022 09:43:13 GMT  
		Size: 17.9 MB (17926654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:8` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:d107e114e807621e44d59e995606b461defa2ef36ec2d254d33a8f3d80382bb7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **731.1 MB (731133977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8cb48dd1921aa0785b96ef5dbede3728d7ab4307ebaa6860be14f63e4c9a07e`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:22 GMT
ADD file:5286ff5db23c42ac6a437e8f2f9ef01b6ee6e523d7866c752428d54f177c7108 in / 
# Wed, 20 Apr 2022 04:29:22 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 08:59:16 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 08:59:36 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 08:59:37 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 08:59:37 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 08:59:41 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:02:54 GMT
ARG LLVM_VERSION=12
# Wed, 20 Apr 2022 09:02:55 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 20 Apr 2022 09:03:05 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 20 Apr 2022 09:05:20 GMT
ARG GHC=8.10.7
# Wed, 20 Apr 2022 09:05:21 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 20 Apr 2022 09:06:32 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:06:33 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:06:34 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:06:35 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:06:35 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:06:36 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b9f330b3a7e234282d632d95bd19a655cf0e06c1a76a51d0f73b9581be8f851b`  
		Last Modified: Wed, 20 Apr 2022 04:36:12 GMT  
		Size: 49.2 MB (49227738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5ee4bd4966ccf295d78d6280d9c6c58bb10c7101e786dad41eca501be7bc3d`  
		Last Modified: Wed, 20 Apr 2022 09:09:35 GMT  
		Size: 114.7 MB (114682952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f32f6654228ae9b68ace1b0f310037fbea0486b4256d01c705c6151d221b6e`  
		Last Modified: Wed, 20 Apr 2022 09:09:24 GMT  
		Size: 17.0 MB (16983880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57285cfdcd6b6a4f817703748a56dca91915beb5991759d627f8315115c9c9da`  
		Last Modified: Wed, 20 Apr 2022 09:12:39 GMT  
		Size: 59.9 MB (59908200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffee208d28f3dc8a7e98abe05e6f2326622d3388a20e91d28b2d92a6600a186`  
		Last Modified: Wed, 20 Apr 2022 09:16:27 GMT  
		Size: 490.3 MB (490331207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8-buster`

```console
$ docker pull haskell@sha256:aaa408ad7e7eff6cd76c39feae223db7ba3550b937e833e78958478334fc9afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:8-buster` - linux; amd64

```console
$ docker pull haskell@sha256:c70ba511d11de63ebcfb93e74b0da327ee9893ef933c87d4514c405d4e087f75
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.5 MB (529538103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7654255acc2e886b1340b582489f7732497d7ce8396edb54b721cd3e0d0dcb`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:37 GMT
ADD file:7c5789fb822bda2652d7addee832c5a3d71733f0f94f97d89b0c5570c0840829 in / 
# Wed, 20 Apr 2022 04:43:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:28:53 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:29:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:29:16 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:29:17 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:29:19 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:32:24 GMT
ARG LLVM_VERSION=12
# Wed, 20 Apr 2022 09:32:24 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 20 Apr 2022 09:32:25 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 20 Apr 2022 09:34:56 GMT
ARG GHC=8.10.7
# Wed, 20 Apr 2022 09:34:56 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 20 Apr 2022 09:35:57 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:36:04 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:36:04 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:36:08 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:36:08 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:36:08 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:85bed84afb9a834cf090b55d2e584abd55b4792d93b750db896f486680638344`  
		Last Modified: Wed, 20 Apr 2022 04:48:49 GMT  
		Size: 50.4 MB (50436985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b522b8c18adf55149c7dd6ddd4becc626f002e805952405cc9904c55e038c4c2`  
		Last Modified: Wed, 20 Apr 2022 09:38:19 GMT  
		Size: 120.6 MB (120639968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bbb5b2ebcc192a387282f0d58027a5e65da5844d39689ac323a0d7192d6e7a`  
		Last Modified: Wed, 20 Apr 2022 09:38:02 GMT  
		Size: 10.0 MB (10032282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4cf90ffbaa9b2eb22b002bc5540ca94e5f7f0382bf6797baf23095f63f7fab`  
		Last Modified: Wed, 20 Apr 2022 09:44:16 GMT  
		Size: 330.5 MB (330502214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0434fc716c3d7af8358295c79b97e856e8effd26893a9abc59eccca76d68f2`  
		Last Modified: Wed, 20 Apr 2022 09:43:13 GMT  
		Size: 17.9 MB (17926654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:8-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:d107e114e807621e44d59e995606b461defa2ef36ec2d254d33a8f3d80382bb7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **731.1 MB (731133977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8cb48dd1921aa0785b96ef5dbede3728d7ab4307ebaa6860be14f63e4c9a07e`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:22 GMT
ADD file:5286ff5db23c42ac6a437e8f2f9ef01b6ee6e523d7866c752428d54f177c7108 in / 
# Wed, 20 Apr 2022 04:29:22 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 08:59:16 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 08:59:36 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 08:59:37 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 08:59:37 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 08:59:41 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:02:54 GMT
ARG LLVM_VERSION=12
# Wed, 20 Apr 2022 09:02:55 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 20 Apr 2022 09:03:05 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 20 Apr 2022 09:05:20 GMT
ARG GHC=8.10.7
# Wed, 20 Apr 2022 09:05:21 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 20 Apr 2022 09:06:32 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:06:33 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:06:34 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:06:35 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:06:35 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:06:36 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b9f330b3a7e234282d632d95bd19a655cf0e06c1a76a51d0f73b9581be8f851b`  
		Last Modified: Wed, 20 Apr 2022 04:36:12 GMT  
		Size: 49.2 MB (49227738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5ee4bd4966ccf295d78d6280d9c6c58bb10c7101e786dad41eca501be7bc3d`  
		Last Modified: Wed, 20 Apr 2022 09:09:35 GMT  
		Size: 114.7 MB (114682952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f32f6654228ae9b68ace1b0f310037fbea0486b4256d01c705c6151d221b6e`  
		Last Modified: Wed, 20 Apr 2022 09:09:24 GMT  
		Size: 17.0 MB (16983880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57285cfdcd6b6a4f817703748a56dca91915beb5991759d627f8315115c9c9da`  
		Last Modified: Wed, 20 Apr 2022 09:12:39 GMT  
		Size: 59.9 MB (59908200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffee208d28f3dc8a7e98abe05e6f2326622d3388a20e91d28b2d92a6600a186`  
		Last Modified: Wed, 20 Apr 2022 09:16:27 GMT  
		Size: 490.3 MB (490331207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8-slim`

```console
$ docker pull haskell@sha256:e5ed447015f4ff4fc60ac3f70e6858a401eb40a7e050b6e2b7c613c333d534b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:8-slim` - linux; amd64

```console
$ docker pull haskell@sha256:a02a9aeb6ceb7616d44a3f0f6ccc5a9a8b3dd74d2e0d1dface8588ee2ae6b925
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.6 MB (363612853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb3ca6c9adc6ceaae6567e45095a0a0409d9ab737ef884e5907c4a052941a9c3`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:30:46 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:31:05 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:31:06 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:31:06 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:31:08 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:33:47 GMT
ARG LLVM_VERSION=12
# Wed, 20 Apr 2022 09:33:47 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 20 Apr 2022 09:33:47 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 20 Apr 2022 09:36:19 GMT
ARG GHC=8.10.7
# Wed, 20 Apr 2022 09:36:19 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 20 Apr 2022 09:37:13 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:37:17 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:37:17 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:37:20 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:37:21 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:37:21 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2614050a0a5f46894d8232687f8437a82fe2d5becd1be0d0e86309b437e8cf`  
		Last Modified: Wed, 20 Apr 2022 09:39:55 GMT  
		Size: 94.0 MB (93994300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c71673cbdf81d2f1ac583fe12755a6ca5820194658d4f1fef0ff70568f798f`  
		Last Modified: Wed, 20 Apr 2022 09:39:43 GMT  
		Size: 10.0 MB (10032281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c8e996eadbd1bd71ca8f7797bfa02ba89f04a58ff396643eab09a7f6ec9d8f3`  
		Last Modified: Wed, 20 Apr 2022 09:45:20 GMT  
		Size: 214.5 MB (214518952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197e9d3d214c1935e7de17738408e167dd8cea3e836188066571a2193f9e981d`  
		Last Modified: Wed, 20 Apr 2022 09:44:41 GMT  
		Size: 17.9 MB (17926656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:8-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:dc67d52766e93b4db2e819f1d98c989c5520d465023868735b2b87153b7a1a8a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.4 MB (515362348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5cae6d3abcac3550d5b3d0259fccd0f0d2466df7ae4d781bb1ebddcb49df07c`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:36 GMT
ADD file:5de4397c1295f7249c93907be599d96efbd9cd25909340d245ec8d1c9770f444 in / 
# Wed, 20 Apr 2022 04:29:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:01:12 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:01:30 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:01:31 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:01:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:01:35 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:04:07 GMT
ARG LLVM_VERSION=12
# Wed, 20 Apr 2022 09:04:08 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 20 Apr 2022 09:04:17 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 20 Apr 2022 09:06:46 GMT
ARG GHC=8.10.7
# Wed, 20 Apr 2022 09:06:47 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 20 Apr 2022 09:07:52 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:07:53 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:07:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:07:55 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:07:56 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:07:57 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6c3e5b218d6477ff77053280968d5bdeaa5dcf16a803e917d98dd0ea8b93ac82`  
		Last Modified: Wed, 20 Apr 2022 04:36:38 GMT  
		Size: 25.9 MB (25908349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5c65fed0b5ed83432918c6a2ad9f45a492561115f67fd6a3cf95ee31e2b52f`  
		Last Modified: Wed, 20 Apr 2022 09:11:22 GMT  
		Size: 88.0 MB (88019933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5f97ca95a1b2683266801fff26205c1a3921ea8d3e1d61980edd259cc77d65`  
		Last Modified: Wed, 20 Apr 2022 09:11:13 GMT  
		Size: 17.0 MB (16983876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16b0eef15e0c3ce60c829cb2886d89908625a1187d78451f4bf5bb857973c751`  
		Last Modified: Wed, 20 Apr 2022 09:13:46 GMT  
		Size: 59.6 MB (59622958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d12d248a1486024255ff924e561c02369629cba9c3f2413867be1001a889bb`  
		Last Modified: Wed, 20 Apr 2022 09:17:59 GMT  
		Size: 324.8 MB (324827232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8-slim-buster`

```console
$ docker pull haskell@sha256:e5ed447015f4ff4fc60ac3f70e6858a401eb40a7e050b6e2b7c613c333d534b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:8-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:a02a9aeb6ceb7616d44a3f0f6ccc5a9a8b3dd74d2e0d1dface8588ee2ae6b925
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.6 MB (363612853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb3ca6c9adc6ceaae6567e45095a0a0409d9ab737ef884e5907c4a052941a9c3`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:30:46 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:31:05 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:31:06 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:31:06 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:31:08 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:33:47 GMT
ARG LLVM_VERSION=12
# Wed, 20 Apr 2022 09:33:47 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 20 Apr 2022 09:33:47 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 20 Apr 2022 09:36:19 GMT
ARG GHC=8.10.7
# Wed, 20 Apr 2022 09:36:19 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 20 Apr 2022 09:37:13 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:37:17 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:37:17 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:37:20 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:37:21 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:37:21 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2614050a0a5f46894d8232687f8437a82fe2d5becd1be0d0e86309b437e8cf`  
		Last Modified: Wed, 20 Apr 2022 09:39:55 GMT  
		Size: 94.0 MB (93994300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c71673cbdf81d2f1ac583fe12755a6ca5820194658d4f1fef0ff70568f798f`  
		Last Modified: Wed, 20 Apr 2022 09:39:43 GMT  
		Size: 10.0 MB (10032281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c8e996eadbd1bd71ca8f7797bfa02ba89f04a58ff396643eab09a7f6ec9d8f3`  
		Last Modified: Wed, 20 Apr 2022 09:45:20 GMT  
		Size: 214.5 MB (214518952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197e9d3d214c1935e7de17738408e167dd8cea3e836188066571a2193f9e981d`  
		Last Modified: Wed, 20 Apr 2022 09:44:41 GMT  
		Size: 17.9 MB (17926656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:8-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:dc67d52766e93b4db2e819f1d98c989c5520d465023868735b2b87153b7a1a8a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.4 MB (515362348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5cae6d3abcac3550d5b3d0259fccd0f0d2466df7ae4d781bb1ebddcb49df07c`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:36 GMT
ADD file:5de4397c1295f7249c93907be599d96efbd9cd25909340d245ec8d1c9770f444 in / 
# Wed, 20 Apr 2022 04:29:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:01:12 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:01:30 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:01:31 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:01:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:01:35 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:04:07 GMT
ARG LLVM_VERSION=12
# Wed, 20 Apr 2022 09:04:08 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 20 Apr 2022 09:04:17 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 20 Apr 2022 09:06:46 GMT
ARG GHC=8.10.7
# Wed, 20 Apr 2022 09:06:47 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 20 Apr 2022 09:07:52 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:07:53 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:07:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:07:55 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:07:56 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:07:57 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6c3e5b218d6477ff77053280968d5bdeaa5dcf16a803e917d98dd0ea8b93ac82`  
		Last Modified: Wed, 20 Apr 2022 04:36:38 GMT  
		Size: 25.9 MB (25908349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5c65fed0b5ed83432918c6a2ad9f45a492561115f67fd6a3cf95ee31e2b52f`  
		Last Modified: Wed, 20 Apr 2022 09:11:22 GMT  
		Size: 88.0 MB (88019933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5f97ca95a1b2683266801fff26205c1a3921ea8d3e1d61980edd259cc77d65`  
		Last Modified: Wed, 20 Apr 2022 09:11:13 GMT  
		Size: 17.0 MB (16983876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16b0eef15e0c3ce60c829cb2886d89908625a1187d78451f4bf5bb857973c751`  
		Last Modified: Wed, 20 Apr 2022 09:13:46 GMT  
		Size: 59.6 MB (59622958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d12d248a1486024255ff924e561c02369629cba9c3f2413867be1001a889bb`  
		Last Modified: Wed, 20 Apr 2022 09:17:59 GMT  
		Size: 324.8 MB (324827232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8.10`

```console
$ docker pull haskell@sha256:aaa408ad7e7eff6cd76c39feae223db7ba3550b937e833e78958478334fc9afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:8.10` - linux; amd64

```console
$ docker pull haskell@sha256:c70ba511d11de63ebcfb93e74b0da327ee9893ef933c87d4514c405d4e087f75
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.5 MB (529538103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7654255acc2e886b1340b582489f7732497d7ce8396edb54b721cd3e0d0dcb`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:37 GMT
ADD file:7c5789fb822bda2652d7addee832c5a3d71733f0f94f97d89b0c5570c0840829 in / 
# Wed, 20 Apr 2022 04:43:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:28:53 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:29:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:29:16 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:29:17 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:29:19 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:32:24 GMT
ARG LLVM_VERSION=12
# Wed, 20 Apr 2022 09:32:24 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 20 Apr 2022 09:32:25 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 20 Apr 2022 09:34:56 GMT
ARG GHC=8.10.7
# Wed, 20 Apr 2022 09:34:56 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 20 Apr 2022 09:35:57 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:36:04 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:36:04 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:36:08 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:36:08 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:36:08 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:85bed84afb9a834cf090b55d2e584abd55b4792d93b750db896f486680638344`  
		Last Modified: Wed, 20 Apr 2022 04:48:49 GMT  
		Size: 50.4 MB (50436985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b522b8c18adf55149c7dd6ddd4becc626f002e805952405cc9904c55e038c4c2`  
		Last Modified: Wed, 20 Apr 2022 09:38:19 GMT  
		Size: 120.6 MB (120639968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bbb5b2ebcc192a387282f0d58027a5e65da5844d39689ac323a0d7192d6e7a`  
		Last Modified: Wed, 20 Apr 2022 09:38:02 GMT  
		Size: 10.0 MB (10032282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4cf90ffbaa9b2eb22b002bc5540ca94e5f7f0382bf6797baf23095f63f7fab`  
		Last Modified: Wed, 20 Apr 2022 09:44:16 GMT  
		Size: 330.5 MB (330502214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0434fc716c3d7af8358295c79b97e856e8effd26893a9abc59eccca76d68f2`  
		Last Modified: Wed, 20 Apr 2022 09:43:13 GMT  
		Size: 17.9 MB (17926654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:8.10` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:d107e114e807621e44d59e995606b461defa2ef36ec2d254d33a8f3d80382bb7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **731.1 MB (731133977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8cb48dd1921aa0785b96ef5dbede3728d7ab4307ebaa6860be14f63e4c9a07e`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:22 GMT
ADD file:5286ff5db23c42ac6a437e8f2f9ef01b6ee6e523d7866c752428d54f177c7108 in / 
# Wed, 20 Apr 2022 04:29:22 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 08:59:16 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 08:59:36 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 08:59:37 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 08:59:37 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 08:59:41 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:02:54 GMT
ARG LLVM_VERSION=12
# Wed, 20 Apr 2022 09:02:55 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 20 Apr 2022 09:03:05 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 20 Apr 2022 09:05:20 GMT
ARG GHC=8.10.7
# Wed, 20 Apr 2022 09:05:21 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 20 Apr 2022 09:06:32 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:06:33 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:06:34 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:06:35 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:06:35 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:06:36 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b9f330b3a7e234282d632d95bd19a655cf0e06c1a76a51d0f73b9581be8f851b`  
		Last Modified: Wed, 20 Apr 2022 04:36:12 GMT  
		Size: 49.2 MB (49227738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5ee4bd4966ccf295d78d6280d9c6c58bb10c7101e786dad41eca501be7bc3d`  
		Last Modified: Wed, 20 Apr 2022 09:09:35 GMT  
		Size: 114.7 MB (114682952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f32f6654228ae9b68ace1b0f310037fbea0486b4256d01c705c6151d221b6e`  
		Last Modified: Wed, 20 Apr 2022 09:09:24 GMT  
		Size: 17.0 MB (16983880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57285cfdcd6b6a4f817703748a56dca91915beb5991759d627f8315115c9c9da`  
		Last Modified: Wed, 20 Apr 2022 09:12:39 GMT  
		Size: 59.9 MB (59908200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffee208d28f3dc8a7e98abe05e6f2326622d3388a20e91d28b2d92a6600a186`  
		Last Modified: Wed, 20 Apr 2022 09:16:27 GMT  
		Size: 490.3 MB (490331207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8.10-buster`

```console
$ docker pull haskell@sha256:aaa408ad7e7eff6cd76c39feae223db7ba3550b937e833e78958478334fc9afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:8.10-buster` - linux; amd64

```console
$ docker pull haskell@sha256:c70ba511d11de63ebcfb93e74b0da327ee9893ef933c87d4514c405d4e087f75
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.5 MB (529538103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7654255acc2e886b1340b582489f7732497d7ce8396edb54b721cd3e0d0dcb`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:37 GMT
ADD file:7c5789fb822bda2652d7addee832c5a3d71733f0f94f97d89b0c5570c0840829 in / 
# Wed, 20 Apr 2022 04:43:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:28:53 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:29:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:29:16 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:29:17 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:29:19 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:32:24 GMT
ARG LLVM_VERSION=12
# Wed, 20 Apr 2022 09:32:24 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 20 Apr 2022 09:32:25 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 20 Apr 2022 09:34:56 GMT
ARG GHC=8.10.7
# Wed, 20 Apr 2022 09:34:56 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 20 Apr 2022 09:35:57 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:36:04 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:36:04 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:36:08 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:36:08 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:36:08 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:85bed84afb9a834cf090b55d2e584abd55b4792d93b750db896f486680638344`  
		Last Modified: Wed, 20 Apr 2022 04:48:49 GMT  
		Size: 50.4 MB (50436985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b522b8c18adf55149c7dd6ddd4becc626f002e805952405cc9904c55e038c4c2`  
		Last Modified: Wed, 20 Apr 2022 09:38:19 GMT  
		Size: 120.6 MB (120639968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bbb5b2ebcc192a387282f0d58027a5e65da5844d39689ac323a0d7192d6e7a`  
		Last Modified: Wed, 20 Apr 2022 09:38:02 GMT  
		Size: 10.0 MB (10032282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4cf90ffbaa9b2eb22b002bc5540ca94e5f7f0382bf6797baf23095f63f7fab`  
		Last Modified: Wed, 20 Apr 2022 09:44:16 GMT  
		Size: 330.5 MB (330502214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0434fc716c3d7af8358295c79b97e856e8effd26893a9abc59eccca76d68f2`  
		Last Modified: Wed, 20 Apr 2022 09:43:13 GMT  
		Size: 17.9 MB (17926654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:8.10-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:d107e114e807621e44d59e995606b461defa2ef36ec2d254d33a8f3d80382bb7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **731.1 MB (731133977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8cb48dd1921aa0785b96ef5dbede3728d7ab4307ebaa6860be14f63e4c9a07e`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:22 GMT
ADD file:5286ff5db23c42ac6a437e8f2f9ef01b6ee6e523d7866c752428d54f177c7108 in / 
# Wed, 20 Apr 2022 04:29:22 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 08:59:16 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 08:59:36 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 08:59:37 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 08:59:37 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 08:59:41 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:02:54 GMT
ARG LLVM_VERSION=12
# Wed, 20 Apr 2022 09:02:55 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 20 Apr 2022 09:03:05 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 20 Apr 2022 09:05:20 GMT
ARG GHC=8.10.7
# Wed, 20 Apr 2022 09:05:21 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 20 Apr 2022 09:06:32 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:06:33 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:06:34 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:06:35 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:06:35 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:06:36 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b9f330b3a7e234282d632d95bd19a655cf0e06c1a76a51d0f73b9581be8f851b`  
		Last Modified: Wed, 20 Apr 2022 04:36:12 GMT  
		Size: 49.2 MB (49227738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5ee4bd4966ccf295d78d6280d9c6c58bb10c7101e786dad41eca501be7bc3d`  
		Last Modified: Wed, 20 Apr 2022 09:09:35 GMT  
		Size: 114.7 MB (114682952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f32f6654228ae9b68ace1b0f310037fbea0486b4256d01c705c6151d221b6e`  
		Last Modified: Wed, 20 Apr 2022 09:09:24 GMT  
		Size: 17.0 MB (16983880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57285cfdcd6b6a4f817703748a56dca91915beb5991759d627f8315115c9c9da`  
		Last Modified: Wed, 20 Apr 2022 09:12:39 GMT  
		Size: 59.9 MB (59908200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffee208d28f3dc8a7e98abe05e6f2326622d3388a20e91d28b2d92a6600a186`  
		Last Modified: Wed, 20 Apr 2022 09:16:27 GMT  
		Size: 490.3 MB (490331207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8.10-slim`

```console
$ docker pull haskell@sha256:e5ed447015f4ff4fc60ac3f70e6858a401eb40a7e050b6e2b7c613c333d534b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:8.10-slim` - linux; amd64

```console
$ docker pull haskell@sha256:a02a9aeb6ceb7616d44a3f0f6ccc5a9a8b3dd74d2e0d1dface8588ee2ae6b925
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.6 MB (363612853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb3ca6c9adc6ceaae6567e45095a0a0409d9ab737ef884e5907c4a052941a9c3`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:30:46 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:31:05 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:31:06 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:31:06 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:31:08 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:33:47 GMT
ARG LLVM_VERSION=12
# Wed, 20 Apr 2022 09:33:47 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 20 Apr 2022 09:33:47 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 20 Apr 2022 09:36:19 GMT
ARG GHC=8.10.7
# Wed, 20 Apr 2022 09:36:19 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 20 Apr 2022 09:37:13 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:37:17 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:37:17 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:37:20 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:37:21 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:37:21 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2614050a0a5f46894d8232687f8437a82fe2d5becd1be0d0e86309b437e8cf`  
		Last Modified: Wed, 20 Apr 2022 09:39:55 GMT  
		Size: 94.0 MB (93994300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c71673cbdf81d2f1ac583fe12755a6ca5820194658d4f1fef0ff70568f798f`  
		Last Modified: Wed, 20 Apr 2022 09:39:43 GMT  
		Size: 10.0 MB (10032281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c8e996eadbd1bd71ca8f7797bfa02ba89f04a58ff396643eab09a7f6ec9d8f3`  
		Last Modified: Wed, 20 Apr 2022 09:45:20 GMT  
		Size: 214.5 MB (214518952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197e9d3d214c1935e7de17738408e167dd8cea3e836188066571a2193f9e981d`  
		Last Modified: Wed, 20 Apr 2022 09:44:41 GMT  
		Size: 17.9 MB (17926656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:8.10-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:dc67d52766e93b4db2e819f1d98c989c5520d465023868735b2b87153b7a1a8a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.4 MB (515362348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5cae6d3abcac3550d5b3d0259fccd0f0d2466df7ae4d781bb1ebddcb49df07c`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:36 GMT
ADD file:5de4397c1295f7249c93907be599d96efbd9cd25909340d245ec8d1c9770f444 in / 
# Wed, 20 Apr 2022 04:29:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:01:12 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:01:30 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:01:31 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:01:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:01:35 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:04:07 GMT
ARG LLVM_VERSION=12
# Wed, 20 Apr 2022 09:04:08 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 20 Apr 2022 09:04:17 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 20 Apr 2022 09:06:46 GMT
ARG GHC=8.10.7
# Wed, 20 Apr 2022 09:06:47 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 20 Apr 2022 09:07:52 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:07:53 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:07:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:07:55 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:07:56 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:07:57 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6c3e5b218d6477ff77053280968d5bdeaa5dcf16a803e917d98dd0ea8b93ac82`  
		Last Modified: Wed, 20 Apr 2022 04:36:38 GMT  
		Size: 25.9 MB (25908349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5c65fed0b5ed83432918c6a2ad9f45a492561115f67fd6a3cf95ee31e2b52f`  
		Last Modified: Wed, 20 Apr 2022 09:11:22 GMT  
		Size: 88.0 MB (88019933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5f97ca95a1b2683266801fff26205c1a3921ea8d3e1d61980edd259cc77d65`  
		Last Modified: Wed, 20 Apr 2022 09:11:13 GMT  
		Size: 17.0 MB (16983876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16b0eef15e0c3ce60c829cb2886d89908625a1187d78451f4bf5bb857973c751`  
		Last Modified: Wed, 20 Apr 2022 09:13:46 GMT  
		Size: 59.6 MB (59622958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d12d248a1486024255ff924e561c02369629cba9c3f2413867be1001a889bb`  
		Last Modified: Wed, 20 Apr 2022 09:17:59 GMT  
		Size: 324.8 MB (324827232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8.10-slim-buster`

```console
$ docker pull haskell@sha256:e5ed447015f4ff4fc60ac3f70e6858a401eb40a7e050b6e2b7c613c333d534b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:8.10-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:a02a9aeb6ceb7616d44a3f0f6ccc5a9a8b3dd74d2e0d1dface8588ee2ae6b925
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.6 MB (363612853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb3ca6c9adc6ceaae6567e45095a0a0409d9ab737ef884e5907c4a052941a9c3`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:30:46 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:31:05 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:31:06 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:31:06 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:31:08 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:33:47 GMT
ARG LLVM_VERSION=12
# Wed, 20 Apr 2022 09:33:47 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 20 Apr 2022 09:33:47 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 20 Apr 2022 09:36:19 GMT
ARG GHC=8.10.7
# Wed, 20 Apr 2022 09:36:19 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 20 Apr 2022 09:37:13 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:37:17 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:37:17 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:37:20 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:37:21 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:37:21 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2614050a0a5f46894d8232687f8437a82fe2d5becd1be0d0e86309b437e8cf`  
		Last Modified: Wed, 20 Apr 2022 09:39:55 GMT  
		Size: 94.0 MB (93994300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c71673cbdf81d2f1ac583fe12755a6ca5820194658d4f1fef0ff70568f798f`  
		Last Modified: Wed, 20 Apr 2022 09:39:43 GMT  
		Size: 10.0 MB (10032281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c8e996eadbd1bd71ca8f7797bfa02ba89f04a58ff396643eab09a7f6ec9d8f3`  
		Last Modified: Wed, 20 Apr 2022 09:45:20 GMT  
		Size: 214.5 MB (214518952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197e9d3d214c1935e7de17738408e167dd8cea3e836188066571a2193f9e981d`  
		Last Modified: Wed, 20 Apr 2022 09:44:41 GMT  
		Size: 17.9 MB (17926656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:8.10-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:dc67d52766e93b4db2e819f1d98c989c5520d465023868735b2b87153b7a1a8a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.4 MB (515362348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5cae6d3abcac3550d5b3d0259fccd0f0d2466df7ae4d781bb1ebddcb49df07c`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:36 GMT
ADD file:5de4397c1295f7249c93907be599d96efbd9cd25909340d245ec8d1c9770f444 in / 
# Wed, 20 Apr 2022 04:29:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:01:12 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:01:30 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:01:31 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:01:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:01:35 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:04:07 GMT
ARG LLVM_VERSION=12
# Wed, 20 Apr 2022 09:04:08 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 20 Apr 2022 09:04:17 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 20 Apr 2022 09:06:46 GMT
ARG GHC=8.10.7
# Wed, 20 Apr 2022 09:06:47 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 20 Apr 2022 09:07:52 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:07:53 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:07:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:07:55 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:07:56 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:07:57 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6c3e5b218d6477ff77053280968d5bdeaa5dcf16a803e917d98dd0ea8b93ac82`  
		Last Modified: Wed, 20 Apr 2022 04:36:38 GMT  
		Size: 25.9 MB (25908349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5c65fed0b5ed83432918c6a2ad9f45a492561115f67fd6a3cf95ee31e2b52f`  
		Last Modified: Wed, 20 Apr 2022 09:11:22 GMT  
		Size: 88.0 MB (88019933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5f97ca95a1b2683266801fff26205c1a3921ea8d3e1d61980edd259cc77d65`  
		Last Modified: Wed, 20 Apr 2022 09:11:13 GMT  
		Size: 17.0 MB (16983876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16b0eef15e0c3ce60c829cb2886d89908625a1187d78451f4bf5bb857973c751`  
		Last Modified: Wed, 20 Apr 2022 09:13:46 GMT  
		Size: 59.6 MB (59622958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d12d248a1486024255ff924e561c02369629cba9c3f2413867be1001a889bb`  
		Last Modified: Wed, 20 Apr 2022 09:17:59 GMT  
		Size: 324.8 MB (324827232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8.10.7`

```console
$ docker pull haskell@sha256:aaa408ad7e7eff6cd76c39feae223db7ba3550b937e833e78958478334fc9afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:8.10.7` - linux; amd64

```console
$ docker pull haskell@sha256:c70ba511d11de63ebcfb93e74b0da327ee9893ef933c87d4514c405d4e087f75
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.5 MB (529538103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7654255acc2e886b1340b582489f7732497d7ce8396edb54b721cd3e0d0dcb`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:37 GMT
ADD file:7c5789fb822bda2652d7addee832c5a3d71733f0f94f97d89b0c5570c0840829 in / 
# Wed, 20 Apr 2022 04:43:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:28:53 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:29:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:29:16 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:29:17 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:29:19 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:32:24 GMT
ARG LLVM_VERSION=12
# Wed, 20 Apr 2022 09:32:24 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 20 Apr 2022 09:32:25 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 20 Apr 2022 09:34:56 GMT
ARG GHC=8.10.7
# Wed, 20 Apr 2022 09:34:56 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 20 Apr 2022 09:35:57 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:36:04 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:36:04 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:36:08 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:36:08 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:36:08 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:85bed84afb9a834cf090b55d2e584abd55b4792d93b750db896f486680638344`  
		Last Modified: Wed, 20 Apr 2022 04:48:49 GMT  
		Size: 50.4 MB (50436985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b522b8c18adf55149c7dd6ddd4becc626f002e805952405cc9904c55e038c4c2`  
		Last Modified: Wed, 20 Apr 2022 09:38:19 GMT  
		Size: 120.6 MB (120639968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bbb5b2ebcc192a387282f0d58027a5e65da5844d39689ac323a0d7192d6e7a`  
		Last Modified: Wed, 20 Apr 2022 09:38:02 GMT  
		Size: 10.0 MB (10032282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4cf90ffbaa9b2eb22b002bc5540ca94e5f7f0382bf6797baf23095f63f7fab`  
		Last Modified: Wed, 20 Apr 2022 09:44:16 GMT  
		Size: 330.5 MB (330502214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0434fc716c3d7af8358295c79b97e856e8effd26893a9abc59eccca76d68f2`  
		Last Modified: Wed, 20 Apr 2022 09:43:13 GMT  
		Size: 17.9 MB (17926654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:8.10.7` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:d107e114e807621e44d59e995606b461defa2ef36ec2d254d33a8f3d80382bb7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **731.1 MB (731133977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8cb48dd1921aa0785b96ef5dbede3728d7ab4307ebaa6860be14f63e4c9a07e`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:22 GMT
ADD file:5286ff5db23c42ac6a437e8f2f9ef01b6ee6e523d7866c752428d54f177c7108 in / 
# Wed, 20 Apr 2022 04:29:22 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 08:59:16 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 08:59:36 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 08:59:37 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 08:59:37 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 08:59:41 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:02:54 GMT
ARG LLVM_VERSION=12
# Wed, 20 Apr 2022 09:02:55 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 20 Apr 2022 09:03:05 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 20 Apr 2022 09:05:20 GMT
ARG GHC=8.10.7
# Wed, 20 Apr 2022 09:05:21 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 20 Apr 2022 09:06:32 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:06:33 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:06:34 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:06:35 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:06:35 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:06:36 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b9f330b3a7e234282d632d95bd19a655cf0e06c1a76a51d0f73b9581be8f851b`  
		Last Modified: Wed, 20 Apr 2022 04:36:12 GMT  
		Size: 49.2 MB (49227738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5ee4bd4966ccf295d78d6280d9c6c58bb10c7101e786dad41eca501be7bc3d`  
		Last Modified: Wed, 20 Apr 2022 09:09:35 GMT  
		Size: 114.7 MB (114682952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f32f6654228ae9b68ace1b0f310037fbea0486b4256d01c705c6151d221b6e`  
		Last Modified: Wed, 20 Apr 2022 09:09:24 GMT  
		Size: 17.0 MB (16983880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57285cfdcd6b6a4f817703748a56dca91915beb5991759d627f8315115c9c9da`  
		Last Modified: Wed, 20 Apr 2022 09:12:39 GMT  
		Size: 59.9 MB (59908200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffee208d28f3dc8a7e98abe05e6f2326622d3388a20e91d28b2d92a6600a186`  
		Last Modified: Wed, 20 Apr 2022 09:16:27 GMT  
		Size: 490.3 MB (490331207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8.10.7-buster`

```console
$ docker pull haskell@sha256:aaa408ad7e7eff6cd76c39feae223db7ba3550b937e833e78958478334fc9afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:8.10.7-buster` - linux; amd64

```console
$ docker pull haskell@sha256:c70ba511d11de63ebcfb93e74b0da327ee9893ef933c87d4514c405d4e087f75
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.5 MB (529538103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7654255acc2e886b1340b582489f7732497d7ce8396edb54b721cd3e0d0dcb`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:37 GMT
ADD file:7c5789fb822bda2652d7addee832c5a3d71733f0f94f97d89b0c5570c0840829 in / 
# Wed, 20 Apr 2022 04:43:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:28:53 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:29:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:29:16 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:29:17 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:29:19 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:32:24 GMT
ARG LLVM_VERSION=12
# Wed, 20 Apr 2022 09:32:24 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 20 Apr 2022 09:32:25 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 20 Apr 2022 09:34:56 GMT
ARG GHC=8.10.7
# Wed, 20 Apr 2022 09:34:56 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 20 Apr 2022 09:35:57 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:36:04 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:36:04 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:36:08 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:36:08 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:36:08 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:85bed84afb9a834cf090b55d2e584abd55b4792d93b750db896f486680638344`  
		Last Modified: Wed, 20 Apr 2022 04:48:49 GMT  
		Size: 50.4 MB (50436985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b522b8c18adf55149c7dd6ddd4becc626f002e805952405cc9904c55e038c4c2`  
		Last Modified: Wed, 20 Apr 2022 09:38:19 GMT  
		Size: 120.6 MB (120639968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bbb5b2ebcc192a387282f0d58027a5e65da5844d39689ac323a0d7192d6e7a`  
		Last Modified: Wed, 20 Apr 2022 09:38:02 GMT  
		Size: 10.0 MB (10032282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4cf90ffbaa9b2eb22b002bc5540ca94e5f7f0382bf6797baf23095f63f7fab`  
		Last Modified: Wed, 20 Apr 2022 09:44:16 GMT  
		Size: 330.5 MB (330502214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0434fc716c3d7af8358295c79b97e856e8effd26893a9abc59eccca76d68f2`  
		Last Modified: Wed, 20 Apr 2022 09:43:13 GMT  
		Size: 17.9 MB (17926654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:8.10.7-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:d107e114e807621e44d59e995606b461defa2ef36ec2d254d33a8f3d80382bb7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **731.1 MB (731133977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8cb48dd1921aa0785b96ef5dbede3728d7ab4307ebaa6860be14f63e4c9a07e`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:22 GMT
ADD file:5286ff5db23c42ac6a437e8f2f9ef01b6ee6e523d7866c752428d54f177c7108 in / 
# Wed, 20 Apr 2022 04:29:22 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 08:59:16 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 08:59:36 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 08:59:37 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 08:59:37 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 08:59:41 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:02:54 GMT
ARG LLVM_VERSION=12
# Wed, 20 Apr 2022 09:02:55 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 20 Apr 2022 09:03:05 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 20 Apr 2022 09:05:20 GMT
ARG GHC=8.10.7
# Wed, 20 Apr 2022 09:05:21 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 20 Apr 2022 09:06:32 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:06:33 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:06:34 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:06:35 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:06:35 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:06:36 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b9f330b3a7e234282d632d95bd19a655cf0e06c1a76a51d0f73b9581be8f851b`  
		Last Modified: Wed, 20 Apr 2022 04:36:12 GMT  
		Size: 49.2 MB (49227738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5ee4bd4966ccf295d78d6280d9c6c58bb10c7101e786dad41eca501be7bc3d`  
		Last Modified: Wed, 20 Apr 2022 09:09:35 GMT  
		Size: 114.7 MB (114682952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f32f6654228ae9b68ace1b0f310037fbea0486b4256d01c705c6151d221b6e`  
		Last Modified: Wed, 20 Apr 2022 09:09:24 GMT  
		Size: 17.0 MB (16983880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57285cfdcd6b6a4f817703748a56dca91915beb5991759d627f8315115c9c9da`  
		Last Modified: Wed, 20 Apr 2022 09:12:39 GMT  
		Size: 59.9 MB (59908200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffee208d28f3dc8a7e98abe05e6f2326622d3388a20e91d28b2d92a6600a186`  
		Last Modified: Wed, 20 Apr 2022 09:16:27 GMT  
		Size: 490.3 MB (490331207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8.10.7-slim`

```console
$ docker pull haskell@sha256:e5ed447015f4ff4fc60ac3f70e6858a401eb40a7e050b6e2b7c613c333d534b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:8.10.7-slim` - linux; amd64

```console
$ docker pull haskell@sha256:a02a9aeb6ceb7616d44a3f0f6ccc5a9a8b3dd74d2e0d1dface8588ee2ae6b925
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.6 MB (363612853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb3ca6c9adc6ceaae6567e45095a0a0409d9ab737ef884e5907c4a052941a9c3`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:30:46 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:31:05 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:31:06 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:31:06 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:31:08 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:33:47 GMT
ARG LLVM_VERSION=12
# Wed, 20 Apr 2022 09:33:47 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 20 Apr 2022 09:33:47 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 20 Apr 2022 09:36:19 GMT
ARG GHC=8.10.7
# Wed, 20 Apr 2022 09:36:19 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 20 Apr 2022 09:37:13 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:37:17 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:37:17 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:37:20 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:37:21 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:37:21 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2614050a0a5f46894d8232687f8437a82fe2d5becd1be0d0e86309b437e8cf`  
		Last Modified: Wed, 20 Apr 2022 09:39:55 GMT  
		Size: 94.0 MB (93994300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c71673cbdf81d2f1ac583fe12755a6ca5820194658d4f1fef0ff70568f798f`  
		Last Modified: Wed, 20 Apr 2022 09:39:43 GMT  
		Size: 10.0 MB (10032281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c8e996eadbd1bd71ca8f7797bfa02ba89f04a58ff396643eab09a7f6ec9d8f3`  
		Last Modified: Wed, 20 Apr 2022 09:45:20 GMT  
		Size: 214.5 MB (214518952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197e9d3d214c1935e7de17738408e167dd8cea3e836188066571a2193f9e981d`  
		Last Modified: Wed, 20 Apr 2022 09:44:41 GMT  
		Size: 17.9 MB (17926656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:8.10.7-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:dc67d52766e93b4db2e819f1d98c989c5520d465023868735b2b87153b7a1a8a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.4 MB (515362348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5cae6d3abcac3550d5b3d0259fccd0f0d2466df7ae4d781bb1ebddcb49df07c`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:36 GMT
ADD file:5de4397c1295f7249c93907be599d96efbd9cd25909340d245ec8d1c9770f444 in / 
# Wed, 20 Apr 2022 04:29:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:01:12 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:01:30 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:01:31 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:01:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:01:35 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:04:07 GMT
ARG LLVM_VERSION=12
# Wed, 20 Apr 2022 09:04:08 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 20 Apr 2022 09:04:17 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 20 Apr 2022 09:06:46 GMT
ARG GHC=8.10.7
# Wed, 20 Apr 2022 09:06:47 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 20 Apr 2022 09:07:52 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:07:53 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:07:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:07:55 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:07:56 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:07:57 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6c3e5b218d6477ff77053280968d5bdeaa5dcf16a803e917d98dd0ea8b93ac82`  
		Last Modified: Wed, 20 Apr 2022 04:36:38 GMT  
		Size: 25.9 MB (25908349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5c65fed0b5ed83432918c6a2ad9f45a492561115f67fd6a3cf95ee31e2b52f`  
		Last Modified: Wed, 20 Apr 2022 09:11:22 GMT  
		Size: 88.0 MB (88019933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5f97ca95a1b2683266801fff26205c1a3921ea8d3e1d61980edd259cc77d65`  
		Last Modified: Wed, 20 Apr 2022 09:11:13 GMT  
		Size: 17.0 MB (16983876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16b0eef15e0c3ce60c829cb2886d89908625a1187d78451f4bf5bb857973c751`  
		Last Modified: Wed, 20 Apr 2022 09:13:46 GMT  
		Size: 59.6 MB (59622958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d12d248a1486024255ff924e561c02369629cba9c3f2413867be1001a889bb`  
		Last Modified: Wed, 20 Apr 2022 09:17:59 GMT  
		Size: 324.8 MB (324827232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8.10.7-slim-buster`

```console
$ docker pull haskell@sha256:e5ed447015f4ff4fc60ac3f70e6858a401eb40a7e050b6e2b7c613c333d534b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:8.10.7-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:a02a9aeb6ceb7616d44a3f0f6ccc5a9a8b3dd74d2e0d1dface8588ee2ae6b925
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.6 MB (363612853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb3ca6c9adc6ceaae6567e45095a0a0409d9ab737ef884e5907c4a052941a9c3`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:30:46 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:31:05 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:31:06 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:31:06 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:31:08 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:33:47 GMT
ARG LLVM_VERSION=12
# Wed, 20 Apr 2022 09:33:47 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 20 Apr 2022 09:33:47 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 20 Apr 2022 09:36:19 GMT
ARG GHC=8.10.7
# Wed, 20 Apr 2022 09:36:19 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 20 Apr 2022 09:37:13 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:37:17 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:37:17 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:37:20 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:37:21 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:37:21 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2614050a0a5f46894d8232687f8437a82fe2d5becd1be0d0e86309b437e8cf`  
		Last Modified: Wed, 20 Apr 2022 09:39:55 GMT  
		Size: 94.0 MB (93994300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c71673cbdf81d2f1ac583fe12755a6ca5820194658d4f1fef0ff70568f798f`  
		Last Modified: Wed, 20 Apr 2022 09:39:43 GMT  
		Size: 10.0 MB (10032281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c8e996eadbd1bd71ca8f7797bfa02ba89f04a58ff396643eab09a7f6ec9d8f3`  
		Last Modified: Wed, 20 Apr 2022 09:45:20 GMT  
		Size: 214.5 MB (214518952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197e9d3d214c1935e7de17738408e167dd8cea3e836188066571a2193f9e981d`  
		Last Modified: Wed, 20 Apr 2022 09:44:41 GMT  
		Size: 17.9 MB (17926656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:8.10.7-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:dc67d52766e93b4db2e819f1d98c989c5520d465023868735b2b87153b7a1a8a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.4 MB (515362348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5cae6d3abcac3550d5b3d0259fccd0f0d2466df7ae4d781bb1ebddcb49df07c`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:36 GMT
ADD file:5de4397c1295f7249c93907be599d96efbd9cd25909340d245ec8d1c9770f444 in / 
# Wed, 20 Apr 2022 04:29:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:01:12 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:01:30 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:01:31 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:01:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:01:35 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:04:07 GMT
ARG LLVM_VERSION=12
# Wed, 20 Apr 2022 09:04:08 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 20 Apr 2022 09:04:17 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 20 Apr 2022 09:06:46 GMT
ARG GHC=8.10.7
# Wed, 20 Apr 2022 09:06:47 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 20 Apr 2022 09:07:52 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:07:53 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:07:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:07:55 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:07:56 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:07:57 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6c3e5b218d6477ff77053280968d5bdeaa5dcf16a803e917d98dd0ea8b93ac82`  
		Last Modified: Wed, 20 Apr 2022 04:36:38 GMT  
		Size: 25.9 MB (25908349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5c65fed0b5ed83432918c6a2ad9f45a492561115f67fd6a3cf95ee31e2b52f`  
		Last Modified: Wed, 20 Apr 2022 09:11:22 GMT  
		Size: 88.0 MB (88019933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5f97ca95a1b2683266801fff26205c1a3921ea8d3e1d61980edd259cc77d65`  
		Last Modified: Wed, 20 Apr 2022 09:11:13 GMT  
		Size: 17.0 MB (16983876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16b0eef15e0c3ce60c829cb2886d89908625a1187d78451f4bf5bb857973c751`  
		Last Modified: Wed, 20 Apr 2022 09:13:46 GMT  
		Size: 59.6 MB (59622958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d12d248a1486024255ff924e561c02369629cba9c3f2413867be1001a889bb`  
		Last Modified: Wed, 20 Apr 2022 09:17:59 GMT  
		Size: 324.8 MB (324827232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9`

```console
$ docker pull haskell@sha256:f99b7e5417f75089b53e1077a68c6333c48b82aff478a8af292a7b7f8e541832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9` - linux; amd64

```console
$ docker pull haskell@sha256:25cdcca5b4cf85e1ac8a73d010f260bfa65c7d4641c727253e82292e0f47fe0a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.1 MB (540052890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02fcce7eeaf2151ffd78b7a37010f74d1faaf6310e25476376964ba31822e6f2`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:37 GMT
ADD file:7c5789fb822bda2652d7addee832c5a3d71733f0f94f97d89b0c5570c0840829 in / 
# Wed, 20 Apr 2022 04:43:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:28:53 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:29:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:29:16 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:29:17 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:29:19 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:29:20 GMT
ARG GHC=9.2.2
# Wed, 20 Apr 2022 09:29:20 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 20 Apr 2022 09:30:25 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:30:32 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:30:32 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:30:36 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:30:36 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:30:36 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:85bed84afb9a834cf090b55d2e584abd55b4792d93b750db896f486680638344`  
		Last Modified: Wed, 20 Apr 2022 04:48:49 GMT  
		Size: 50.4 MB (50436985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b522b8c18adf55149c7dd6ddd4becc626f002e805952405cc9904c55e038c4c2`  
		Last Modified: Wed, 20 Apr 2022 09:38:19 GMT  
		Size: 120.6 MB (120639968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bbb5b2ebcc192a387282f0d58027a5e65da5844d39689ac323a0d7192d6e7a`  
		Last Modified: Wed, 20 Apr 2022 09:38:02 GMT  
		Size: 10.0 MB (10032282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6c2e9e6a17b4aaf841639cfb346e31ed6887458f506e32e6e407371822fbff`  
		Last Modified: Wed, 20 Apr 2022 09:39:08 GMT  
		Size: 341.0 MB (341017006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37705d98ee41cfe0ebbac02e738ee2c630b751a9f2779fa0eb22a623a0ce6406`  
		Last Modified: Wed, 20 Apr 2022 09:38:04 GMT  
		Size: 17.9 MB (17926649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:103a94c87cf5679f23c2477e9fd11e1f7077f1740ba71b9e8aad797f68dc0c18
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.6 MB (586552265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:356a1d587827e5f83f872cedb3bb173889426295d950a044ac5b1d1ee1357d80`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:22 GMT
ADD file:5286ff5db23c42ac6a437e8f2f9ef01b6ee6e523d7866c752428d54f177c7108 in / 
# Wed, 20 Apr 2022 04:29:22 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 08:59:16 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 08:59:36 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 08:59:37 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 08:59:37 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 08:59:41 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 08:59:41 GMT
ARG GHC=9.2.2
# Wed, 20 Apr 2022 08:59:42 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 20 Apr 2022 09:00:52 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:00:53 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:00:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:00:55 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:00:56 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:00:56 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b9f330b3a7e234282d632d95bd19a655cf0e06c1a76a51d0f73b9581be8f851b`  
		Last Modified: Wed, 20 Apr 2022 04:36:12 GMT  
		Size: 49.2 MB (49227738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5ee4bd4966ccf295d78d6280d9c6c58bb10c7101e786dad41eca501be7bc3d`  
		Last Modified: Wed, 20 Apr 2022 09:09:35 GMT  
		Size: 114.7 MB (114682952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f32f6654228ae9b68ace1b0f310037fbea0486b4256d01c705c6151d221b6e`  
		Last Modified: Wed, 20 Apr 2022 09:09:24 GMT  
		Size: 17.0 MB (16983880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71d8f04ee288260f5c56be044c8d3df485ab4d58aee98283c06b940762e12d8`  
		Last Modified: Wed, 20 Apr 2022 09:10:41 GMT  
		Size: 405.7 MB (405657695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9-buster`

```console
$ docker pull haskell@sha256:f99b7e5417f75089b53e1077a68c6333c48b82aff478a8af292a7b7f8e541832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9-buster` - linux; amd64

```console
$ docker pull haskell@sha256:25cdcca5b4cf85e1ac8a73d010f260bfa65c7d4641c727253e82292e0f47fe0a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.1 MB (540052890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02fcce7eeaf2151ffd78b7a37010f74d1faaf6310e25476376964ba31822e6f2`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:37 GMT
ADD file:7c5789fb822bda2652d7addee832c5a3d71733f0f94f97d89b0c5570c0840829 in / 
# Wed, 20 Apr 2022 04:43:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:28:53 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:29:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:29:16 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:29:17 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:29:19 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:29:20 GMT
ARG GHC=9.2.2
# Wed, 20 Apr 2022 09:29:20 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 20 Apr 2022 09:30:25 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:30:32 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:30:32 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:30:36 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:30:36 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:30:36 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:85bed84afb9a834cf090b55d2e584abd55b4792d93b750db896f486680638344`  
		Last Modified: Wed, 20 Apr 2022 04:48:49 GMT  
		Size: 50.4 MB (50436985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b522b8c18adf55149c7dd6ddd4becc626f002e805952405cc9904c55e038c4c2`  
		Last Modified: Wed, 20 Apr 2022 09:38:19 GMT  
		Size: 120.6 MB (120639968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bbb5b2ebcc192a387282f0d58027a5e65da5844d39689ac323a0d7192d6e7a`  
		Last Modified: Wed, 20 Apr 2022 09:38:02 GMT  
		Size: 10.0 MB (10032282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6c2e9e6a17b4aaf841639cfb346e31ed6887458f506e32e6e407371822fbff`  
		Last Modified: Wed, 20 Apr 2022 09:39:08 GMT  
		Size: 341.0 MB (341017006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37705d98ee41cfe0ebbac02e738ee2c630b751a9f2779fa0eb22a623a0ce6406`  
		Last Modified: Wed, 20 Apr 2022 09:38:04 GMT  
		Size: 17.9 MB (17926649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:103a94c87cf5679f23c2477e9fd11e1f7077f1740ba71b9e8aad797f68dc0c18
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.6 MB (586552265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:356a1d587827e5f83f872cedb3bb173889426295d950a044ac5b1d1ee1357d80`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:22 GMT
ADD file:5286ff5db23c42ac6a437e8f2f9ef01b6ee6e523d7866c752428d54f177c7108 in / 
# Wed, 20 Apr 2022 04:29:22 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 08:59:16 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 08:59:36 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 08:59:37 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 08:59:37 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 08:59:41 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 08:59:41 GMT
ARG GHC=9.2.2
# Wed, 20 Apr 2022 08:59:42 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 20 Apr 2022 09:00:52 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:00:53 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:00:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:00:55 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:00:56 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:00:56 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b9f330b3a7e234282d632d95bd19a655cf0e06c1a76a51d0f73b9581be8f851b`  
		Last Modified: Wed, 20 Apr 2022 04:36:12 GMT  
		Size: 49.2 MB (49227738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5ee4bd4966ccf295d78d6280d9c6c58bb10c7101e786dad41eca501be7bc3d`  
		Last Modified: Wed, 20 Apr 2022 09:09:35 GMT  
		Size: 114.7 MB (114682952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f32f6654228ae9b68ace1b0f310037fbea0486b4256d01c705c6151d221b6e`  
		Last Modified: Wed, 20 Apr 2022 09:09:24 GMT  
		Size: 17.0 MB (16983880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71d8f04ee288260f5c56be044c8d3df485ab4d58aee98283c06b940762e12d8`  
		Last Modified: Wed, 20 Apr 2022 09:10:41 GMT  
		Size: 405.7 MB (405657695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9-slim`

```console
$ docker pull haskell@sha256:7252508f81c0e0a05f93727969f44ceafa3f7188bc53bed8f44e48b4160295cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9-slim` - linux; amd64

```console
$ docker pull haskell@sha256:5f15f23eeb9c2c4db14fa0e1e5d2a770a6a024114aa9e0e11d2db2a6d216ce96
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.2 MB (368220347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810fded7b58e5a381c4220c438ece5b79f93f1a069da0c233052fde981ebca31`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:30:46 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:31:05 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:31:06 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:31:06 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:31:08 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:31:09 GMT
ARG GHC=9.2.2
# Wed, 20 Apr 2022 09:31:09 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 20 Apr 2022 09:32:05 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:32:09 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:32:09 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:32:12 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:32:12 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:32:12 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2614050a0a5f46894d8232687f8437a82fe2d5becd1be0d0e86309b437e8cf`  
		Last Modified: Wed, 20 Apr 2022 09:39:55 GMT  
		Size: 94.0 MB (93994300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c71673cbdf81d2f1ac583fe12755a6ca5820194658d4f1fef0ff70568f798f`  
		Last Modified: Wed, 20 Apr 2022 09:39:43 GMT  
		Size: 10.0 MB (10032281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4203c687a2c1f84741fd0c89a57f821d6e4b3e917e2d0135e059e5f983b20b19`  
		Last Modified: Wed, 20 Apr 2022 09:40:25 GMT  
		Size: 219.1 MB (219126455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24c61b185e6c468d5348e50c481053315d6cd79b1ba16d4c9f921a0cfaa896e`  
		Last Modified: Wed, 20 Apr 2022 09:39:44 GMT  
		Size: 17.9 MB (17926647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:65b2614cf4553c59da1e6e89a69ec66381313f124509423d0c95d62f2b20d89c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.9 MB (391852184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025a295bdb9f1d5eff4ee739f75787e4f66d15581141a4fc6fc98ff2f4d9a683`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:36 GMT
ADD file:5de4397c1295f7249c93907be599d96efbd9cd25909340d245ec8d1c9770f444 in / 
# Wed, 20 Apr 2022 04:29:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:01:12 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:01:30 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:01:31 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:01:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:01:35 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:01:35 GMT
ARG GHC=9.2.2
# Wed, 20 Apr 2022 09:01:36 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 20 Apr 2022 09:02:41 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:02:41 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:02:42 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:02:43 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:02:44 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:02:45 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6c3e5b218d6477ff77053280968d5bdeaa5dcf16a803e917d98dd0ea8b93ac82`  
		Last Modified: Wed, 20 Apr 2022 04:36:38 GMT  
		Size: 25.9 MB (25908349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5c65fed0b5ed83432918c6a2ad9f45a492561115f67fd6a3cf95ee31e2b52f`  
		Last Modified: Wed, 20 Apr 2022 09:11:22 GMT  
		Size: 88.0 MB (88019933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5f97ca95a1b2683266801fff26205c1a3921ea8d3e1d61980edd259cc77d65`  
		Last Modified: Wed, 20 Apr 2022 09:11:13 GMT  
		Size: 17.0 MB (16983876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f9af39df7c7bb928d2f8fa1b872b53cc164f5171b1e446372248960cf3637b`  
		Last Modified: Wed, 20 Apr 2022 09:12:03 GMT  
		Size: 260.9 MB (260940026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9-slim-buster`

```console
$ docker pull haskell@sha256:7252508f81c0e0a05f93727969f44ceafa3f7188bc53bed8f44e48b4160295cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:5f15f23eeb9c2c4db14fa0e1e5d2a770a6a024114aa9e0e11d2db2a6d216ce96
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.2 MB (368220347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810fded7b58e5a381c4220c438ece5b79f93f1a069da0c233052fde981ebca31`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:30:46 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:31:05 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:31:06 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:31:06 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:31:08 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:31:09 GMT
ARG GHC=9.2.2
# Wed, 20 Apr 2022 09:31:09 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 20 Apr 2022 09:32:05 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:32:09 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:32:09 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:32:12 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:32:12 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:32:12 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2614050a0a5f46894d8232687f8437a82fe2d5becd1be0d0e86309b437e8cf`  
		Last Modified: Wed, 20 Apr 2022 09:39:55 GMT  
		Size: 94.0 MB (93994300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c71673cbdf81d2f1ac583fe12755a6ca5820194658d4f1fef0ff70568f798f`  
		Last Modified: Wed, 20 Apr 2022 09:39:43 GMT  
		Size: 10.0 MB (10032281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4203c687a2c1f84741fd0c89a57f821d6e4b3e917e2d0135e059e5f983b20b19`  
		Last Modified: Wed, 20 Apr 2022 09:40:25 GMT  
		Size: 219.1 MB (219126455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24c61b185e6c468d5348e50c481053315d6cd79b1ba16d4c9f921a0cfaa896e`  
		Last Modified: Wed, 20 Apr 2022 09:39:44 GMT  
		Size: 17.9 MB (17926647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:65b2614cf4553c59da1e6e89a69ec66381313f124509423d0c95d62f2b20d89c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.9 MB (391852184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025a295bdb9f1d5eff4ee739f75787e4f66d15581141a4fc6fc98ff2f4d9a683`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:36 GMT
ADD file:5de4397c1295f7249c93907be599d96efbd9cd25909340d245ec8d1c9770f444 in / 
# Wed, 20 Apr 2022 04:29:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:01:12 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:01:30 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:01:31 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:01:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:01:35 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:01:35 GMT
ARG GHC=9.2.2
# Wed, 20 Apr 2022 09:01:36 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 20 Apr 2022 09:02:41 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:02:41 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:02:42 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:02:43 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:02:44 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:02:45 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6c3e5b218d6477ff77053280968d5bdeaa5dcf16a803e917d98dd0ea8b93ac82`  
		Last Modified: Wed, 20 Apr 2022 04:36:38 GMT  
		Size: 25.9 MB (25908349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5c65fed0b5ed83432918c6a2ad9f45a492561115f67fd6a3cf95ee31e2b52f`  
		Last Modified: Wed, 20 Apr 2022 09:11:22 GMT  
		Size: 88.0 MB (88019933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5f97ca95a1b2683266801fff26205c1a3921ea8d3e1d61980edd259cc77d65`  
		Last Modified: Wed, 20 Apr 2022 09:11:13 GMT  
		Size: 17.0 MB (16983876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f9af39df7c7bb928d2f8fa1b872b53cc164f5171b1e446372248960cf3637b`  
		Last Modified: Wed, 20 Apr 2022 09:12:03 GMT  
		Size: 260.9 MB (260940026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0`

```console
$ docker pull haskell@sha256:5d9e8d5e169e94a03a720a3a208aa31e509fe3c2b6232085eed48fbf52be6770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.0` - linux; amd64

```console
$ docker pull haskell@sha256:714396bc21a3eef683fbbe9729e41d9b0d0bab094a946cb05217715cf6609c96
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.5 MB (525452282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370b9ed7ae3cd9db88b33a738c508711a3684ff79ac081afa4fb050e66df184e`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:37 GMT
ADD file:7c5789fb822bda2652d7addee832c5a3d71733f0f94f97d89b0c5570c0840829 in / 
# Wed, 20 Apr 2022 04:43:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:28:53 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:29:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:29:16 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:29:17 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:29:19 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:32:24 GMT
ARG LLVM_VERSION=12
# Wed, 20 Apr 2022 09:32:24 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 20 Apr 2022 09:32:25 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 20 Apr 2022 09:32:25 GMT
ARG GHC=9.0.2
# Wed, 20 Apr 2022 09:32:25 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 20 Apr 2022 09:33:31 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:33:38 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:33:38 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:33:41 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:33:41 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:33:41 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:85bed84afb9a834cf090b55d2e584abd55b4792d93b750db896f486680638344`  
		Last Modified: Wed, 20 Apr 2022 04:48:49 GMT  
		Size: 50.4 MB (50436985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b522b8c18adf55149c7dd6ddd4becc626f002e805952405cc9904c55e038c4c2`  
		Last Modified: Wed, 20 Apr 2022 09:38:19 GMT  
		Size: 120.6 MB (120639968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bbb5b2ebcc192a387282f0d58027a5e65da5844d39689ac323a0d7192d6e7a`  
		Last Modified: Wed, 20 Apr 2022 09:38:02 GMT  
		Size: 10.0 MB (10032282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bac936c1c4f37f3d72f9fc21ed7e9de8fed3a84793c93468dd804f093117efd`  
		Last Modified: Wed, 20 Apr 2022 09:41:56 GMT  
		Size: 326.4 MB (326416395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf42fcf4126ca95d062e3c8b1db7a1a1429cf8b74ee1b12351ba0f2a69fa418e`  
		Last Modified: Wed, 20 Apr 2022 09:40:55 GMT  
		Size: 17.9 MB (17926652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.0` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:0e05c44bd73e7524993b843b021c4d031ac756d1274a4cab5b65ae15477723dc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **471.8 MB (471787237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bba4cf2912834d613cb4bf3cef4e7083e1ed7f9edb387b3b25bc2048a08bd3fa`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:22 GMT
ADD file:5286ff5db23c42ac6a437e8f2f9ef01b6ee6e523d7866c752428d54f177c7108 in / 
# Wed, 20 Apr 2022 04:29:22 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 08:59:16 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 08:59:36 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 08:59:37 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 08:59:37 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 08:59:41 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:02:54 GMT
ARG LLVM_VERSION=12
# Wed, 20 Apr 2022 09:02:55 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 20 Apr 2022 09:03:05 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 20 Apr 2022 09:03:06 GMT
ARG GHC=9.0.2
# Wed, 20 Apr 2022 09:03:06 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 20 Apr 2022 09:03:56 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:03:57 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:03:58 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:03:59 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:04:00 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:04:00 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b9f330b3a7e234282d632d95bd19a655cf0e06c1a76a51d0f73b9581be8f851b`  
		Last Modified: Wed, 20 Apr 2022 04:36:12 GMT  
		Size: 49.2 MB (49227738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5ee4bd4966ccf295d78d6280d9c6c58bb10c7101e786dad41eca501be7bc3d`  
		Last Modified: Wed, 20 Apr 2022 09:09:35 GMT  
		Size: 114.7 MB (114682952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f32f6654228ae9b68ace1b0f310037fbea0486b4256d01c705c6151d221b6e`  
		Last Modified: Wed, 20 Apr 2022 09:09:24 GMT  
		Size: 17.0 MB (16983880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57285cfdcd6b6a4f817703748a56dca91915beb5991759d627f8315115c9c9da`  
		Last Modified: Wed, 20 Apr 2022 09:12:39 GMT  
		Size: 59.9 MB (59908200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e68bb731950f4e88894356ac97c2b444d802c63c64429b44625e09bb5f293bd`  
		Last Modified: Wed, 20 Apr 2022 09:13:20 GMT  
		Size: 231.0 MB (230984467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0-buster`

```console
$ docker pull haskell@sha256:5d9e8d5e169e94a03a720a3a208aa31e509fe3c2b6232085eed48fbf52be6770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.0-buster` - linux; amd64

```console
$ docker pull haskell@sha256:714396bc21a3eef683fbbe9729e41d9b0d0bab094a946cb05217715cf6609c96
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.5 MB (525452282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370b9ed7ae3cd9db88b33a738c508711a3684ff79ac081afa4fb050e66df184e`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:37 GMT
ADD file:7c5789fb822bda2652d7addee832c5a3d71733f0f94f97d89b0c5570c0840829 in / 
# Wed, 20 Apr 2022 04:43:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:28:53 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:29:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:29:16 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:29:17 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:29:19 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:32:24 GMT
ARG LLVM_VERSION=12
# Wed, 20 Apr 2022 09:32:24 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 20 Apr 2022 09:32:25 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 20 Apr 2022 09:32:25 GMT
ARG GHC=9.0.2
# Wed, 20 Apr 2022 09:32:25 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 20 Apr 2022 09:33:31 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:33:38 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:33:38 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:33:41 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:33:41 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:33:41 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:85bed84afb9a834cf090b55d2e584abd55b4792d93b750db896f486680638344`  
		Last Modified: Wed, 20 Apr 2022 04:48:49 GMT  
		Size: 50.4 MB (50436985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b522b8c18adf55149c7dd6ddd4becc626f002e805952405cc9904c55e038c4c2`  
		Last Modified: Wed, 20 Apr 2022 09:38:19 GMT  
		Size: 120.6 MB (120639968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bbb5b2ebcc192a387282f0d58027a5e65da5844d39689ac323a0d7192d6e7a`  
		Last Modified: Wed, 20 Apr 2022 09:38:02 GMT  
		Size: 10.0 MB (10032282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bac936c1c4f37f3d72f9fc21ed7e9de8fed3a84793c93468dd804f093117efd`  
		Last Modified: Wed, 20 Apr 2022 09:41:56 GMT  
		Size: 326.4 MB (326416395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf42fcf4126ca95d062e3c8b1db7a1a1429cf8b74ee1b12351ba0f2a69fa418e`  
		Last Modified: Wed, 20 Apr 2022 09:40:55 GMT  
		Size: 17.9 MB (17926652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.0-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:0e05c44bd73e7524993b843b021c4d031ac756d1274a4cab5b65ae15477723dc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **471.8 MB (471787237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bba4cf2912834d613cb4bf3cef4e7083e1ed7f9edb387b3b25bc2048a08bd3fa`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:22 GMT
ADD file:5286ff5db23c42ac6a437e8f2f9ef01b6ee6e523d7866c752428d54f177c7108 in / 
# Wed, 20 Apr 2022 04:29:22 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 08:59:16 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 08:59:36 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 08:59:37 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 08:59:37 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 08:59:41 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:02:54 GMT
ARG LLVM_VERSION=12
# Wed, 20 Apr 2022 09:02:55 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 20 Apr 2022 09:03:05 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 20 Apr 2022 09:03:06 GMT
ARG GHC=9.0.2
# Wed, 20 Apr 2022 09:03:06 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 20 Apr 2022 09:03:56 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:03:57 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:03:58 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:03:59 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:04:00 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:04:00 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b9f330b3a7e234282d632d95bd19a655cf0e06c1a76a51d0f73b9581be8f851b`  
		Last Modified: Wed, 20 Apr 2022 04:36:12 GMT  
		Size: 49.2 MB (49227738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5ee4bd4966ccf295d78d6280d9c6c58bb10c7101e786dad41eca501be7bc3d`  
		Last Modified: Wed, 20 Apr 2022 09:09:35 GMT  
		Size: 114.7 MB (114682952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f32f6654228ae9b68ace1b0f310037fbea0486b4256d01c705c6151d221b6e`  
		Last Modified: Wed, 20 Apr 2022 09:09:24 GMT  
		Size: 17.0 MB (16983880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57285cfdcd6b6a4f817703748a56dca91915beb5991759d627f8315115c9c9da`  
		Last Modified: Wed, 20 Apr 2022 09:12:39 GMT  
		Size: 59.9 MB (59908200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e68bb731950f4e88894356ac97c2b444d802c63c64429b44625e09bb5f293bd`  
		Last Modified: Wed, 20 Apr 2022 09:13:20 GMT  
		Size: 231.0 MB (230984467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0-slim`

```console
$ docker pull haskell@sha256:79b03f2b9b25290718aa5412b2df526e925f784aadfc45d4f64b3ab25153c083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.0-slim` - linux; amd64

```console
$ docker pull haskell@sha256:c87a81254857596fd9a0ab302c2b39c40f7a021ce7a99512e629ee3979131ff3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.1 MB (359065031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b17c98035708629dc179c48fe5e4d62e18b7d7bb7892dca21a330d5a8abd23`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:30:46 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:31:05 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:31:06 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:31:06 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:31:08 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:33:47 GMT
ARG LLVM_VERSION=12
# Wed, 20 Apr 2022 09:33:47 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 20 Apr 2022 09:33:47 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 20 Apr 2022 09:33:48 GMT
ARG GHC=9.0.2
# Wed, 20 Apr 2022 09:33:48 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 20 Apr 2022 09:34:46 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:34:50 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:34:50 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:34:53 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:34:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:34:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2614050a0a5f46894d8232687f8437a82fe2d5becd1be0d0e86309b437e8cf`  
		Last Modified: Wed, 20 Apr 2022 09:39:55 GMT  
		Size: 94.0 MB (93994300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c71673cbdf81d2f1ac583fe12755a6ca5820194658d4f1fef0ff70568f798f`  
		Last Modified: Wed, 20 Apr 2022 09:39:43 GMT  
		Size: 10.0 MB (10032281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9fd1e6ce2fa99646af17b3ee4d6d22861fb7258540f6d8adf547dad026068f1`  
		Last Modified: Wed, 20 Apr 2022 09:42:54 GMT  
		Size: 210.0 MB (209971136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e37be5b32469ac133185f187cf3aeedac373e0271d835ca581e9d33a7079d7cd`  
		Last Modified: Wed, 20 Apr 2022 09:42:16 GMT  
		Size: 17.9 MB (17926650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.0-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:a31a55c2b8c0e9f1820d3d365fbcf5c6e0dea7fb38a725b0e6699a44a180f5db
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.5 MB (421519994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:470d9d0ae363aafe03f483b2b49fec602f4bafce7ec9c6399012471cc035664d`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:36 GMT
ADD file:5de4397c1295f7249c93907be599d96efbd9cd25909340d245ec8d1c9770f444 in / 
# Wed, 20 Apr 2022 04:29:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:01:12 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:01:30 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:01:31 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:01:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:01:35 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:04:07 GMT
ARG LLVM_VERSION=12
# Wed, 20 Apr 2022 09:04:08 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 20 Apr 2022 09:04:17 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 20 Apr 2022 09:04:17 GMT
ARG GHC=9.0.2
# Wed, 20 Apr 2022 09:04:18 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 20 Apr 2022 09:05:04 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:05:05 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:05:05 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:05:06 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:05:07 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:05:08 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6c3e5b218d6477ff77053280968d5bdeaa5dcf16a803e917d98dd0ea8b93ac82`  
		Last Modified: Wed, 20 Apr 2022 04:36:38 GMT  
		Size: 25.9 MB (25908349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5c65fed0b5ed83432918c6a2ad9f45a492561115f67fd6a3cf95ee31e2b52f`  
		Last Modified: Wed, 20 Apr 2022 09:11:22 GMT  
		Size: 88.0 MB (88019933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5f97ca95a1b2683266801fff26205c1a3921ea8d3e1d61980edd259cc77d65`  
		Last Modified: Wed, 20 Apr 2022 09:11:13 GMT  
		Size: 17.0 MB (16983876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16b0eef15e0c3ce60c829cb2886d89908625a1187d78451f4bf5bb857973c751`  
		Last Modified: Wed, 20 Apr 2022 09:13:46 GMT  
		Size: 59.6 MB (59622958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16715d9219f124c5f2b920412da9b37e4cce040fc2d6cd55f5e070a794bf6a73`  
		Last Modified: Wed, 20 Apr 2022 09:14:28 GMT  
		Size: 231.0 MB (230984878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0-slim-buster`

```console
$ docker pull haskell@sha256:79b03f2b9b25290718aa5412b2df526e925f784aadfc45d4f64b3ab25153c083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.0-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:c87a81254857596fd9a0ab302c2b39c40f7a021ce7a99512e629ee3979131ff3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.1 MB (359065031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b17c98035708629dc179c48fe5e4d62e18b7d7bb7892dca21a330d5a8abd23`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:30:46 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:31:05 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:31:06 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:31:06 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:31:08 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:33:47 GMT
ARG LLVM_VERSION=12
# Wed, 20 Apr 2022 09:33:47 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 20 Apr 2022 09:33:47 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 20 Apr 2022 09:33:48 GMT
ARG GHC=9.0.2
# Wed, 20 Apr 2022 09:33:48 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 20 Apr 2022 09:34:46 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:34:50 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:34:50 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:34:53 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:34:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:34:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2614050a0a5f46894d8232687f8437a82fe2d5becd1be0d0e86309b437e8cf`  
		Last Modified: Wed, 20 Apr 2022 09:39:55 GMT  
		Size: 94.0 MB (93994300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c71673cbdf81d2f1ac583fe12755a6ca5820194658d4f1fef0ff70568f798f`  
		Last Modified: Wed, 20 Apr 2022 09:39:43 GMT  
		Size: 10.0 MB (10032281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9fd1e6ce2fa99646af17b3ee4d6d22861fb7258540f6d8adf547dad026068f1`  
		Last Modified: Wed, 20 Apr 2022 09:42:54 GMT  
		Size: 210.0 MB (209971136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e37be5b32469ac133185f187cf3aeedac373e0271d835ca581e9d33a7079d7cd`  
		Last Modified: Wed, 20 Apr 2022 09:42:16 GMT  
		Size: 17.9 MB (17926650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.0-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:a31a55c2b8c0e9f1820d3d365fbcf5c6e0dea7fb38a725b0e6699a44a180f5db
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.5 MB (421519994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:470d9d0ae363aafe03f483b2b49fec602f4bafce7ec9c6399012471cc035664d`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:36 GMT
ADD file:5de4397c1295f7249c93907be599d96efbd9cd25909340d245ec8d1c9770f444 in / 
# Wed, 20 Apr 2022 04:29:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:01:12 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:01:30 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:01:31 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:01:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:01:35 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:04:07 GMT
ARG LLVM_VERSION=12
# Wed, 20 Apr 2022 09:04:08 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 20 Apr 2022 09:04:17 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 20 Apr 2022 09:04:17 GMT
ARG GHC=9.0.2
# Wed, 20 Apr 2022 09:04:18 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 20 Apr 2022 09:05:04 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:05:05 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:05:05 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:05:06 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:05:07 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:05:08 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6c3e5b218d6477ff77053280968d5bdeaa5dcf16a803e917d98dd0ea8b93ac82`  
		Last Modified: Wed, 20 Apr 2022 04:36:38 GMT  
		Size: 25.9 MB (25908349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5c65fed0b5ed83432918c6a2ad9f45a492561115f67fd6a3cf95ee31e2b52f`  
		Last Modified: Wed, 20 Apr 2022 09:11:22 GMT  
		Size: 88.0 MB (88019933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5f97ca95a1b2683266801fff26205c1a3921ea8d3e1d61980edd259cc77d65`  
		Last Modified: Wed, 20 Apr 2022 09:11:13 GMT  
		Size: 17.0 MB (16983876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16b0eef15e0c3ce60c829cb2886d89908625a1187d78451f4bf5bb857973c751`  
		Last Modified: Wed, 20 Apr 2022 09:13:46 GMT  
		Size: 59.6 MB (59622958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16715d9219f124c5f2b920412da9b37e4cce040fc2d6cd55f5e070a794bf6a73`  
		Last Modified: Wed, 20 Apr 2022 09:14:28 GMT  
		Size: 231.0 MB (230984878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0.2`

```console
$ docker pull haskell@sha256:5d9e8d5e169e94a03a720a3a208aa31e509fe3c2b6232085eed48fbf52be6770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.0.2` - linux; amd64

```console
$ docker pull haskell@sha256:714396bc21a3eef683fbbe9729e41d9b0d0bab094a946cb05217715cf6609c96
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.5 MB (525452282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370b9ed7ae3cd9db88b33a738c508711a3684ff79ac081afa4fb050e66df184e`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:37 GMT
ADD file:7c5789fb822bda2652d7addee832c5a3d71733f0f94f97d89b0c5570c0840829 in / 
# Wed, 20 Apr 2022 04:43:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:28:53 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:29:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:29:16 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:29:17 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:29:19 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:32:24 GMT
ARG LLVM_VERSION=12
# Wed, 20 Apr 2022 09:32:24 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 20 Apr 2022 09:32:25 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 20 Apr 2022 09:32:25 GMT
ARG GHC=9.0.2
# Wed, 20 Apr 2022 09:32:25 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 20 Apr 2022 09:33:31 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:33:38 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:33:38 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:33:41 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:33:41 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:33:41 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:85bed84afb9a834cf090b55d2e584abd55b4792d93b750db896f486680638344`  
		Last Modified: Wed, 20 Apr 2022 04:48:49 GMT  
		Size: 50.4 MB (50436985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b522b8c18adf55149c7dd6ddd4becc626f002e805952405cc9904c55e038c4c2`  
		Last Modified: Wed, 20 Apr 2022 09:38:19 GMT  
		Size: 120.6 MB (120639968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bbb5b2ebcc192a387282f0d58027a5e65da5844d39689ac323a0d7192d6e7a`  
		Last Modified: Wed, 20 Apr 2022 09:38:02 GMT  
		Size: 10.0 MB (10032282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bac936c1c4f37f3d72f9fc21ed7e9de8fed3a84793c93468dd804f093117efd`  
		Last Modified: Wed, 20 Apr 2022 09:41:56 GMT  
		Size: 326.4 MB (326416395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf42fcf4126ca95d062e3c8b1db7a1a1429cf8b74ee1b12351ba0f2a69fa418e`  
		Last Modified: Wed, 20 Apr 2022 09:40:55 GMT  
		Size: 17.9 MB (17926652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.0.2` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:0e05c44bd73e7524993b843b021c4d031ac756d1274a4cab5b65ae15477723dc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **471.8 MB (471787237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bba4cf2912834d613cb4bf3cef4e7083e1ed7f9edb387b3b25bc2048a08bd3fa`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:22 GMT
ADD file:5286ff5db23c42ac6a437e8f2f9ef01b6ee6e523d7866c752428d54f177c7108 in / 
# Wed, 20 Apr 2022 04:29:22 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 08:59:16 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 08:59:36 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 08:59:37 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 08:59:37 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 08:59:41 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:02:54 GMT
ARG LLVM_VERSION=12
# Wed, 20 Apr 2022 09:02:55 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 20 Apr 2022 09:03:05 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 20 Apr 2022 09:03:06 GMT
ARG GHC=9.0.2
# Wed, 20 Apr 2022 09:03:06 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 20 Apr 2022 09:03:56 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:03:57 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:03:58 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:03:59 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:04:00 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:04:00 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b9f330b3a7e234282d632d95bd19a655cf0e06c1a76a51d0f73b9581be8f851b`  
		Last Modified: Wed, 20 Apr 2022 04:36:12 GMT  
		Size: 49.2 MB (49227738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5ee4bd4966ccf295d78d6280d9c6c58bb10c7101e786dad41eca501be7bc3d`  
		Last Modified: Wed, 20 Apr 2022 09:09:35 GMT  
		Size: 114.7 MB (114682952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f32f6654228ae9b68ace1b0f310037fbea0486b4256d01c705c6151d221b6e`  
		Last Modified: Wed, 20 Apr 2022 09:09:24 GMT  
		Size: 17.0 MB (16983880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57285cfdcd6b6a4f817703748a56dca91915beb5991759d627f8315115c9c9da`  
		Last Modified: Wed, 20 Apr 2022 09:12:39 GMT  
		Size: 59.9 MB (59908200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e68bb731950f4e88894356ac97c2b444d802c63c64429b44625e09bb5f293bd`  
		Last Modified: Wed, 20 Apr 2022 09:13:20 GMT  
		Size: 231.0 MB (230984467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0.2-buster`

```console
$ docker pull haskell@sha256:5d9e8d5e169e94a03a720a3a208aa31e509fe3c2b6232085eed48fbf52be6770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.0.2-buster` - linux; amd64

```console
$ docker pull haskell@sha256:714396bc21a3eef683fbbe9729e41d9b0d0bab094a946cb05217715cf6609c96
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.5 MB (525452282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370b9ed7ae3cd9db88b33a738c508711a3684ff79ac081afa4fb050e66df184e`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:37 GMT
ADD file:7c5789fb822bda2652d7addee832c5a3d71733f0f94f97d89b0c5570c0840829 in / 
# Wed, 20 Apr 2022 04:43:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:28:53 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:29:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:29:16 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:29:17 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:29:19 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:32:24 GMT
ARG LLVM_VERSION=12
# Wed, 20 Apr 2022 09:32:24 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 20 Apr 2022 09:32:25 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 20 Apr 2022 09:32:25 GMT
ARG GHC=9.0.2
# Wed, 20 Apr 2022 09:32:25 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 20 Apr 2022 09:33:31 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:33:38 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:33:38 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:33:41 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:33:41 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:33:41 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:85bed84afb9a834cf090b55d2e584abd55b4792d93b750db896f486680638344`  
		Last Modified: Wed, 20 Apr 2022 04:48:49 GMT  
		Size: 50.4 MB (50436985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b522b8c18adf55149c7dd6ddd4becc626f002e805952405cc9904c55e038c4c2`  
		Last Modified: Wed, 20 Apr 2022 09:38:19 GMT  
		Size: 120.6 MB (120639968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bbb5b2ebcc192a387282f0d58027a5e65da5844d39689ac323a0d7192d6e7a`  
		Last Modified: Wed, 20 Apr 2022 09:38:02 GMT  
		Size: 10.0 MB (10032282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bac936c1c4f37f3d72f9fc21ed7e9de8fed3a84793c93468dd804f093117efd`  
		Last Modified: Wed, 20 Apr 2022 09:41:56 GMT  
		Size: 326.4 MB (326416395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf42fcf4126ca95d062e3c8b1db7a1a1429cf8b74ee1b12351ba0f2a69fa418e`  
		Last Modified: Wed, 20 Apr 2022 09:40:55 GMT  
		Size: 17.9 MB (17926652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.0.2-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:0e05c44bd73e7524993b843b021c4d031ac756d1274a4cab5b65ae15477723dc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **471.8 MB (471787237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bba4cf2912834d613cb4bf3cef4e7083e1ed7f9edb387b3b25bc2048a08bd3fa`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:22 GMT
ADD file:5286ff5db23c42ac6a437e8f2f9ef01b6ee6e523d7866c752428d54f177c7108 in / 
# Wed, 20 Apr 2022 04:29:22 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 08:59:16 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 08:59:36 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 08:59:37 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 08:59:37 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 08:59:41 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:02:54 GMT
ARG LLVM_VERSION=12
# Wed, 20 Apr 2022 09:02:55 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 20 Apr 2022 09:03:05 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 20 Apr 2022 09:03:06 GMT
ARG GHC=9.0.2
# Wed, 20 Apr 2022 09:03:06 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 20 Apr 2022 09:03:56 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:03:57 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:03:58 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:03:59 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:04:00 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:04:00 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b9f330b3a7e234282d632d95bd19a655cf0e06c1a76a51d0f73b9581be8f851b`  
		Last Modified: Wed, 20 Apr 2022 04:36:12 GMT  
		Size: 49.2 MB (49227738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5ee4bd4966ccf295d78d6280d9c6c58bb10c7101e786dad41eca501be7bc3d`  
		Last Modified: Wed, 20 Apr 2022 09:09:35 GMT  
		Size: 114.7 MB (114682952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f32f6654228ae9b68ace1b0f310037fbea0486b4256d01c705c6151d221b6e`  
		Last Modified: Wed, 20 Apr 2022 09:09:24 GMT  
		Size: 17.0 MB (16983880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57285cfdcd6b6a4f817703748a56dca91915beb5991759d627f8315115c9c9da`  
		Last Modified: Wed, 20 Apr 2022 09:12:39 GMT  
		Size: 59.9 MB (59908200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e68bb731950f4e88894356ac97c2b444d802c63c64429b44625e09bb5f293bd`  
		Last Modified: Wed, 20 Apr 2022 09:13:20 GMT  
		Size: 231.0 MB (230984467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0.2-slim`

```console
$ docker pull haskell@sha256:79b03f2b9b25290718aa5412b2df526e925f784aadfc45d4f64b3ab25153c083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.0.2-slim` - linux; amd64

```console
$ docker pull haskell@sha256:c87a81254857596fd9a0ab302c2b39c40f7a021ce7a99512e629ee3979131ff3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.1 MB (359065031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b17c98035708629dc179c48fe5e4d62e18b7d7bb7892dca21a330d5a8abd23`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:30:46 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:31:05 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:31:06 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:31:06 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:31:08 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:33:47 GMT
ARG LLVM_VERSION=12
# Wed, 20 Apr 2022 09:33:47 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 20 Apr 2022 09:33:47 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 20 Apr 2022 09:33:48 GMT
ARG GHC=9.0.2
# Wed, 20 Apr 2022 09:33:48 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 20 Apr 2022 09:34:46 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:34:50 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:34:50 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:34:53 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:34:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:34:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2614050a0a5f46894d8232687f8437a82fe2d5becd1be0d0e86309b437e8cf`  
		Last Modified: Wed, 20 Apr 2022 09:39:55 GMT  
		Size: 94.0 MB (93994300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c71673cbdf81d2f1ac583fe12755a6ca5820194658d4f1fef0ff70568f798f`  
		Last Modified: Wed, 20 Apr 2022 09:39:43 GMT  
		Size: 10.0 MB (10032281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9fd1e6ce2fa99646af17b3ee4d6d22861fb7258540f6d8adf547dad026068f1`  
		Last Modified: Wed, 20 Apr 2022 09:42:54 GMT  
		Size: 210.0 MB (209971136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e37be5b32469ac133185f187cf3aeedac373e0271d835ca581e9d33a7079d7cd`  
		Last Modified: Wed, 20 Apr 2022 09:42:16 GMT  
		Size: 17.9 MB (17926650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.0.2-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:a31a55c2b8c0e9f1820d3d365fbcf5c6e0dea7fb38a725b0e6699a44a180f5db
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.5 MB (421519994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:470d9d0ae363aafe03f483b2b49fec602f4bafce7ec9c6399012471cc035664d`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:36 GMT
ADD file:5de4397c1295f7249c93907be599d96efbd9cd25909340d245ec8d1c9770f444 in / 
# Wed, 20 Apr 2022 04:29:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:01:12 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:01:30 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:01:31 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:01:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:01:35 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:04:07 GMT
ARG LLVM_VERSION=12
# Wed, 20 Apr 2022 09:04:08 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 20 Apr 2022 09:04:17 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 20 Apr 2022 09:04:17 GMT
ARG GHC=9.0.2
# Wed, 20 Apr 2022 09:04:18 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 20 Apr 2022 09:05:04 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:05:05 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:05:05 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:05:06 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:05:07 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:05:08 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6c3e5b218d6477ff77053280968d5bdeaa5dcf16a803e917d98dd0ea8b93ac82`  
		Last Modified: Wed, 20 Apr 2022 04:36:38 GMT  
		Size: 25.9 MB (25908349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5c65fed0b5ed83432918c6a2ad9f45a492561115f67fd6a3cf95ee31e2b52f`  
		Last Modified: Wed, 20 Apr 2022 09:11:22 GMT  
		Size: 88.0 MB (88019933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5f97ca95a1b2683266801fff26205c1a3921ea8d3e1d61980edd259cc77d65`  
		Last Modified: Wed, 20 Apr 2022 09:11:13 GMT  
		Size: 17.0 MB (16983876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16b0eef15e0c3ce60c829cb2886d89908625a1187d78451f4bf5bb857973c751`  
		Last Modified: Wed, 20 Apr 2022 09:13:46 GMT  
		Size: 59.6 MB (59622958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16715d9219f124c5f2b920412da9b37e4cce040fc2d6cd55f5e070a794bf6a73`  
		Last Modified: Wed, 20 Apr 2022 09:14:28 GMT  
		Size: 231.0 MB (230984878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0.2-slim-buster`

```console
$ docker pull haskell@sha256:79b03f2b9b25290718aa5412b2df526e925f784aadfc45d4f64b3ab25153c083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.0.2-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:c87a81254857596fd9a0ab302c2b39c40f7a021ce7a99512e629ee3979131ff3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.1 MB (359065031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b17c98035708629dc179c48fe5e4d62e18b7d7bb7892dca21a330d5a8abd23`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:30:46 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:31:05 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:31:06 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:31:06 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:31:08 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:33:47 GMT
ARG LLVM_VERSION=12
# Wed, 20 Apr 2022 09:33:47 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 20 Apr 2022 09:33:47 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 20 Apr 2022 09:33:48 GMT
ARG GHC=9.0.2
# Wed, 20 Apr 2022 09:33:48 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 20 Apr 2022 09:34:46 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:34:50 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:34:50 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:34:53 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:34:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:34:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2614050a0a5f46894d8232687f8437a82fe2d5becd1be0d0e86309b437e8cf`  
		Last Modified: Wed, 20 Apr 2022 09:39:55 GMT  
		Size: 94.0 MB (93994300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c71673cbdf81d2f1ac583fe12755a6ca5820194658d4f1fef0ff70568f798f`  
		Last Modified: Wed, 20 Apr 2022 09:39:43 GMT  
		Size: 10.0 MB (10032281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9fd1e6ce2fa99646af17b3ee4d6d22861fb7258540f6d8adf547dad026068f1`  
		Last Modified: Wed, 20 Apr 2022 09:42:54 GMT  
		Size: 210.0 MB (209971136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e37be5b32469ac133185f187cf3aeedac373e0271d835ca581e9d33a7079d7cd`  
		Last Modified: Wed, 20 Apr 2022 09:42:16 GMT  
		Size: 17.9 MB (17926650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.0.2-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:a31a55c2b8c0e9f1820d3d365fbcf5c6e0dea7fb38a725b0e6699a44a180f5db
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.5 MB (421519994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:470d9d0ae363aafe03f483b2b49fec602f4bafce7ec9c6399012471cc035664d`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:36 GMT
ADD file:5de4397c1295f7249c93907be599d96efbd9cd25909340d245ec8d1c9770f444 in / 
# Wed, 20 Apr 2022 04:29:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:01:12 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:01:30 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:01:31 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:01:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:01:35 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:04:07 GMT
ARG LLVM_VERSION=12
# Wed, 20 Apr 2022 09:04:08 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 20 Apr 2022 09:04:17 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 20 Apr 2022 09:04:17 GMT
ARG GHC=9.0.2
# Wed, 20 Apr 2022 09:04:18 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 20 Apr 2022 09:05:04 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:05:05 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:05:05 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:05:06 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:05:07 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:05:08 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6c3e5b218d6477ff77053280968d5bdeaa5dcf16a803e917d98dd0ea8b93ac82`  
		Last Modified: Wed, 20 Apr 2022 04:36:38 GMT  
		Size: 25.9 MB (25908349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5c65fed0b5ed83432918c6a2ad9f45a492561115f67fd6a3cf95ee31e2b52f`  
		Last Modified: Wed, 20 Apr 2022 09:11:22 GMT  
		Size: 88.0 MB (88019933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5f97ca95a1b2683266801fff26205c1a3921ea8d3e1d61980edd259cc77d65`  
		Last Modified: Wed, 20 Apr 2022 09:11:13 GMT  
		Size: 17.0 MB (16983876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16b0eef15e0c3ce60c829cb2886d89908625a1187d78451f4bf5bb857973c751`  
		Last Modified: Wed, 20 Apr 2022 09:13:46 GMT  
		Size: 59.6 MB (59622958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16715d9219f124c5f2b920412da9b37e4cce040fc2d6cd55f5e070a794bf6a73`  
		Last Modified: Wed, 20 Apr 2022 09:14:28 GMT  
		Size: 231.0 MB (230984878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.2`

```console
$ docker pull haskell@sha256:f99b7e5417f75089b53e1077a68c6333c48b82aff478a8af292a7b7f8e541832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.2` - linux; amd64

```console
$ docker pull haskell@sha256:25cdcca5b4cf85e1ac8a73d010f260bfa65c7d4641c727253e82292e0f47fe0a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.1 MB (540052890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02fcce7eeaf2151ffd78b7a37010f74d1faaf6310e25476376964ba31822e6f2`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:37 GMT
ADD file:7c5789fb822bda2652d7addee832c5a3d71733f0f94f97d89b0c5570c0840829 in / 
# Wed, 20 Apr 2022 04:43:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:28:53 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:29:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:29:16 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:29:17 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:29:19 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:29:20 GMT
ARG GHC=9.2.2
# Wed, 20 Apr 2022 09:29:20 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 20 Apr 2022 09:30:25 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:30:32 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:30:32 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:30:36 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:30:36 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:30:36 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:85bed84afb9a834cf090b55d2e584abd55b4792d93b750db896f486680638344`  
		Last Modified: Wed, 20 Apr 2022 04:48:49 GMT  
		Size: 50.4 MB (50436985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b522b8c18adf55149c7dd6ddd4becc626f002e805952405cc9904c55e038c4c2`  
		Last Modified: Wed, 20 Apr 2022 09:38:19 GMT  
		Size: 120.6 MB (120639968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bbb5b2ebcc192a387282f0d58027a5e65da5844d39689ac323a0d7192d6e7a`  
		Last Modified: Wed, 20 Apr 2022 09:38:02 GMT  
		Size: 10.0 MB (10032282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6c2e9e6a17b4aaf841639cfb346e31ed6887458f506e32e6e407371822fbff`  
		Last Modified: Wed, 20 Apr 2022 09:39:08 GMT  
		Size: 341.0 MB (341017006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37705d98ee41cfe0ebbac02e738ee2c630b751a9f2779fa0eb22a623a0ce6406`  
		Last Modified: Wed, 20 Apr 2022 09:38:04 GMT  
		Size: 17.9 MB (17926649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.2` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:103a94c87cf5679f23c2477e9fd11e1f7077f1740ba71b9e8aad797f68dc0c18
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.6 MB (586552265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:356a1d587827e5f83f872cedb3bb173889426295d950a044ac5b1d1ee1357d80`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:22 GMT
ADD file:5286ff5db23c42ac6a437e8f2f9ef01b6ee6e523d7866c752428d54f177c7108 in / 
# Wed, 20 Apr 2022 04:29:22 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 08:59:16 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 08:59:36 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 08:59:37 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 08:59:37 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 08:59:41 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 08:59:41 GMT
ARG GHC=9.2.2
# Wed, 20 Apr 2022 08:59:42 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 20 Apr 2022 09:00:52 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:00:53 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:00:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:00:55 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:00:56 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:00:56 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b9f330b3a7e234282d632d95bd19a655cf0e06c1a76a51d0f73b9581be8f851b`  
		Last Modified: Wed, 20 Apr 2022 04:36:12 GMT  
		Size: 49.2 MB (49227738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5ee4bd4966ccf295d78d6280d9c6c58bb10c7101e786dad41eca501be7bc3d`  
		Last Modified: Wed, 20 Apr 2022 09:09:35 GMT  
		Size: 114.7 MB (114682952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f32f6654228ae9b68ace1b0f310037fbea0486b4256d01c705c6151d221b6e`  
		Last Modified: Wed, 20 Apr 2022 09:09:24 GMT  
		Size: 17.0 MB (16983880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71d8f04ee288260f5c56be044c8d3df485ab4d58aee98283c06b940762e12d8`  
		Last Modified: Wed, 20 Apr 2022 09:10:41 GMT  
		Size: 405.7 MB (405657695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.2-buster`

```console
$ docker pull haskell@sha256:f99b7e5417f75089b53e1077a68c6333c48b82aff478a8af292a7b7f8e541832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.2-buster` - linux; amd64

```console
$ docker pull haskell@sha256:25cdcca5b4cf85e1ac8a73d010f260bfa65c7d4641c727253e82292e0f47fe0a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.1 MB (540052890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02fcce7eeaf2151ffd78b7a37010f74d1faaf6310e25476376964ba31822e6f2`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:37 GMT
ADD file:7c5789fb822bda2652d7addee832c5a3d71733f0f94f97d89b0c5570c0840829 in / 
# Wed, 20 Apr 2022 04:43:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:28:53 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:29:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:29:16 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:29:17 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:29:19 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:29:20 GMT
ARG GHC=9.2.2
# Wed, 20 Apr 2022 09:29:20 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 20 Apr 2022 09:30:25 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:30:32 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:30:32 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:30:36 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:30:36 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:30:36 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:85bed84afb9a834cf090b55d2e584abd55b4792d93b750db896f486680638344`  
		Last Modified: Wed, 20 Apr 2022 04:48:49 GMT  
		Size: 50.4 MB (50436985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b522b8c18adf55149c7dd6ddd4becc626f002e805952405cc9904c55e038c4c2`  
		Last Modified: Wed, 20 Apr 2022 09:38:19 GMT  
		Size: 120.6 MB (120639968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bbb5b2ebcc192a387282f0d58027a5e65da5844d39689ac323a0d7192d6e7a`  
		Last Modified: Wed, 20 Apr 2022 09:38:02 GMT  
		Size: 10.0 MB (10032282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6c2e9e6a17b4aaf841639cfb346e31ed6887458f506e32e6e407371822fbff`  
		Last Modified: Wed, 20 Apr 2022 09:39:08 GMT  
		Size: 341.0 MB (341017006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37705d98ee41cfe0ebbac02e738ee2c630b751a9f2779fa0eb22a623a0ce6406`  
		Last Modified: Wed, 20 Apr 2022 09:38:04 GMT  
		Size: 17.9 MB (17926649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.2-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:103a94c87cf5679f23c2477e9fd11e1f7077f1740ba71b9e8aad797f68dc0c18
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.6 MB (586552265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:356a1d587827e5f83f872cedb3bb173889426295d950a044ac5b1d1ee1357d80`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:22 GMT
ADD file:5286ff5db23c42ac6a437e8f2f9ef01b6ee6e523d7866c752428d54f177c7108 in / 
# Wed, 20 Apr 2022 04:29:22 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 08:59:16 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 08:59:36 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 08:59:37 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 08:59:37 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 08:59:41 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 08:59:41 GMT
ARG GHC=9.2.2
# Wed, 20 Apr 2022 08:59:42 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 20 Apr 2022 09:00:52 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:00:53 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:00:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:00:55 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:00:56 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:00:56 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b9f330b3a7e234282d632d95bd19a655cf0e06c1a76a51d0f73b9581be8f851b`  
		Last Modified: Wed, 20 Apr 2022 04:36:12 GMT  
		Size: 49.2 MB (49227738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5ee4bd4966ccf295d78d6280d9c6c58bb10c7101e786dad41eca501be7bc3d`  
		Last Modified: Wed, 20 Apr 2022 09:09:35 GMT  
		Size: 114.7 MB (114682952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f32f6654228ae9b68ace1b0f310037fbea0486b4256d01c705c6151d221b6e`  
		Last Modified: Wed, 20 Apr 2022 09:09:24 GMT  
		Size: 17.0 MB (16983880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71d8f04ee288260f5c56be044c8d3df485ab4d58aee98283c06b940762e12d8`  
		Last Modified: Wed, 20 Apr 2022 09:10:41 GMT  
		Size: 405.7 MB (405657695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.2-slim`

```console
$ docker pull haskell@sha256:7252508f81c0e0a05f93727969f44ceafa3f7188bc53bed8f44e48b4160295cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.2-slim` - linux; amd64

```console
$ docker pull haskell@sha256:5f15f23eeb9c2c4db14fa0e1e5d2a770a6a024114aa9e0e11d2db2a6d216ce96
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.2 MB (368220347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810fded7b58e5a381c4220c438ece5b79f93f1a069da0c233052fde981ebca31`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:30:46 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:31:05 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:31:06 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:31:06 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:31:08 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:31:09 GMT
ARG GHC=9.2.2
# Wed, 20 Apr 2022 09:31:09 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 20 Apr 2022 09:32:05 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:32:09 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:32:09 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:32:12 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:32:12 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:32:12 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2614050a0a5f46894d8232687f8437a82fe2d5becd1be0d0e86309b437e8cf`  
		Last Modified: Wed, 20 Apr 2022 09:39:55 GMT  
		Size: 94.0 MB (93994300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c71673cbdf81d2f1ac583fe12755a6ca5820194658d4f1fef0ff70568f798f`  
		Last Modified: Wed, 20 Apr 2022 09:39:43 GMT  
		Size: 10.0 MB (10032281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4203c687a2c1f84741fd0c89a57f821d6e4b3e917e2d0135e059e5f983b20b19`  
		Last Modified: Wed, 20 Apr 2022 09:40:25 GMT  
		Size: 219.1 MB (219126455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24c61b185e6c468d5348e50c481053315d6cd79b1ba16d4c9f921a0cfaa896e`  
		Last Modified: Wed, 20 Apr 2022 09:39:44 GMT  
		Size: 17.9 MB (17926647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.2-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:65b2614cf4553c59da1e6e89a69ec66381313f124509423d0c95d62f2b20d89c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.9 MB (391852184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025a295bdb9f1d5eff4ee739f75787e4f66d15581141a4fc6fc98ff2f4d9a683`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:36 GMT
ADD file:5de4397c1295f7249c93907be599d96efbd9cd25909340d245ec8d1c9770f444 in / 
# Wed, 20 Apr 2022 04:29:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:01:12 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:01:30 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:01:31 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:01:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:01:35 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:01:35 GMT
ARG GHC=9.2.2
# Wed, 20 Apr 2022 09:01:36 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 20 Apr 2022 09:02:41 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:02:41 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:02:42 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:02:43 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:02:44 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:02:45 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6c3e5b218d6477ff77053280968d5bdeaa5dcf16a803e917d98dd0ea8b93ac82`  
		Last Modified: Wed, 20 Apr 2022 04:36:38 GMT  
		Size: 25.9 MB (25908349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5c65fed0b5ed83432918c6a2ad9f45a492561115f67fd6a3cf95ee31e2b52f`  
		Last Modified: Wed, 20 Apr 2022 09:11:22 GMT  
		Size: 88.0 MB (88019933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5f97ca95a1b2683266801fff26205c1a3921ea8d3e1d61980edd259cc77d65`  
		Last Modified: Wed, 20 Apr 2022 09:11:13 GMT  
		Size: 17.0 MB (16983876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f9af39df7c7bb928d2f8fa1b872b53cc164f5171b1e446372248960cf3637b`  
		Last Modified: Wed, 20 Apr 2022 09:12:03 GMT  
		Size: 260.9 MB (260940026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.2-slim-buster`

```console
$ docker pull haskell@sha256:7252508f81c0e0a05f93727969f44ceafa3f7188bc53bed8f44e48b4160295cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.2-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:5f15f23eeb9c2c4db14fa0e1e5d2a770a6a024114aa9e0e11d2db2a6d216ce96
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.2 MB (368220347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810fded7b58e5a381c4220c438ece5b79f93f1a069da0c233052fde981ebca31`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:30:46 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:31:05 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:31:06 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:31:06 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:31:08 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:31:09 GMT
ARG GHC=9.2.2
# Wed, 20 Apr 2022 09:31:09 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 20 Apr 2022 09:32:05 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:32:09 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:32:09 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:32:12 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:32:12 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:32:12 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2614050a0a5f46894d8232687f8437a82fe2d5becd1be0d0e86309b437e8cf`  
		Last Modified: Wed, 20 Apr 2022 09:39:55 GMT  
		Size: 94.0 MB (93994300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c71673cbdf81d2f1ac583fe12755a6ca5820194658d4f1fef0ff70568f798f`  
		Last Modified: Wed, 20 Apr 2022 09:39:43 GMT  
		Size: 10.0 MB (10032281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4203c687a2c1f84741fd0c89a57f821d6e4b3e917e2d0135e059e5f983b20b19`  
		Last Modified: Wed, 20 Apr 2022 09:40:25 GMT  
		Size: 219.1 MB (219126455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24c61b185e6c468d5348e50c481053315d6cd79b1ba16d4c9f921a0cfaa896e`  
		Last Modified: Wed, 20 Apr 2022 09:39:44 GMT  
		Size: 17.9 MB (17926647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.2-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:65b2614cf4553c59da1e6e89a69ec66381313f124509423d0c95d62f2b20d89c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.9 MB (391852184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025a295bdb9f1d5eff4ee739f75787e4f66d15581141a4fc6fc98ff2f4d9a683`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:36 GMT
ADD file:5de4397c1295f7249c93907be599d96efbd9cd25909340d245ec8d1c9770f444 in / 
# Wed, 20 Apr 2022 04:29:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:01:12 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:01:30 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:01:31 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:01:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:01:35 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:01:35 GMT
ARG GHC=9.2.2
# Wed, 20 Apr 2022 09:01:36 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 20 Apr 2022 09:02:41 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:02:41 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:02:42 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:02:43 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:02:44 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:02:45 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6c3e5b218d6477ff77053280968d5bdeaa5dcf16a803e917d98dd0ea8b93ac82`  
		Last Modified: Wed, 20 Apr 2022 04:36:38 GMT  
		Size: 25.9 MB (25908349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5c65fed0b5ed83432918c6a2ad9f45a492561115f67fd6a3cf95ee31e2b52f`  
		Last Modified: Wed, 20 Apr 2022 09:11:22 GMT  
		Size: 88.0 MB (88019933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5f97ca95a1b2683266801fff26205c1a3921ea8d3e1d61980edd259cc77d65`  
		Last Modified: Wed, 20 Apr 2022 09:11:13 GMT  
		Size: 17.0 MB (16983876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f9af39df7c7bb928d2f8fa1b872b53cc164f5171b1e446372248960cf3637b`  
		Last Modified: Wed, 20 Apr 2022 09:12:03 GMT  
		Size: 260.9 MB (260940026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.2.2`

```console
$ docker pull haskell@sha256:f99b7e5417f75089b53e1077a68c6333c48b82aff478a8af292a7b7f8e541832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.2.2` - linux; amd64

```console
$ docker pull haskell@sha256:25cdcca5b4cf85e1ac8a73d010f260bfa65c7d4641c727253e82292e0f47fe0a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.1 MB (540052890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02fcce7eeaf2151ffd78b7a37010f74d1faaf6310e25476376964ba31822e6f2`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:37 GMT
ADD file:7c5789fb822bda2652d7addee832c5a3d71733f0f94f97d89b0c5570c0840829 in / 
# Wed, 20 Apr 2022 04:43:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:28:53 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:29:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:29:16 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:29:17 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:29:19 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:29:20 GMT
ARG GHC=9.2.2
# Wed, 20 Apr 2022 09:29:20 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 20 Apr 2022 09:30:25 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:30:32 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:30:32 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:30:36 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:30:36 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:30:36 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:85bed84afb9a834cf090b55d2e584abd55b4792d93b750db896f486680638344`  
		Last Modified: Wed, 20 Apr 2022 04:48:49 GMT  
		Size: 50.4 MB (50436985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b522b8c18adf55149c7dd6ddd4becc626f002e805952405cc9904c55e038c4c2`  
		Last Modified: Wed, 20 Apr 2022 09:38:19 GMT  
		Size: 120.6 MB (120639968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bbb5b2ebcc192a387282f0d58027a5e65da5844d39689ac323a0d7192d6e7a`  
		Last Modified: Wed, 20 Apr 2022 09:38:02 GMT  
		Size: 10.0 MB (10032282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6c2e9e6a17b4aaf841639cfb346e31ed6887458f506e32e6e407371822fbff`  
		Last Modified: Wed, 20 Apr 2022 09:39:08 GMT  
		Size: 341.0 MB (341017006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37705d98ee41cfe0ebbac02e738ee2c630b751a9f2779fa0eb22a623a0ce6406`  
		Last Modified: Wed, 20 Apr 2022 09:38:04 GMT  
		Size: 17.9 MB (17926649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.2.2` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:103a94c87cf5679f23c2477e9fd11e1f7077f1740ba71b9e8aad797f68dc0c18
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.6 MB (586552265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:356a1d587827e5f83f872cedb3bb173889426295d950a044ac5b1d1ee1357d80`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:22 GMT
ADD file:5286ff5db23c42ac6a437e8f2f9ef01b6ee6e523d7866c752428d54f177c7108 in / 
# Wed, 20 Apr 2022 04:29:22 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 08:59:16 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 08:59:36 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 08:59:37 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 08:59:37 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 08:59:41 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 08:59:41 GMT
ARG GHC=9.2.2
# Wed, 20 Apr 2022 08:59:42 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 20 Apr 2022 09:00:52 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:00:53 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:00:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:00:55 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:00:56 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:00:56 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b9f330b3a7e234282d632d95bd19a655cf0e06c1a76a51d0f73b9581be8f851b`  
		Last Modified: Wed, 20 Apr 2022 04:36:12 GMT  
		Size: 49.2 MB (49227738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5ee4bd4966ccf295d78d6280d9c6c58bb10c7101e786dad41eca501be7bc3d`  
		Last Modified: Wed, 20 Apr 2022 09:09:35 GMT  
		Size: 114.7 MB (114682952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f32f6654228ae9b68ace1b0f310037fbea0486b4256d01c705c6151d221b6e`  
		Last Modified: Wed, 20 Apr 2022 09:09:24 GMT  
		Size: 17.0 MB (16983880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71d8f04ee288260f5c56be044c8d3df485ab4d58aee98283c06b940762e12d8`  
		Last Modified: Wed, 20 Apr 2022 09:10:41 GMT  
		Size: 405.7 MB (405657695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.2.2-buster`

```console
$ docker pull haskell@sha256:f99b7e5417f75089b53e1077a68c6333c48b82aff478a8af292a7b7f8e541832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.2.2-buster` - linux; amd64

```console
$ docker pull haskell@sha256:25cdcca5b4cf85e1ac8a73d010f260bfa65c7d4641c727253e82292e0f47fe0a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.1 MB (540052890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02fcce7eeaf2151ffd78b7a37010f74d1faaf6310e25476376964ba31822e6f2`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:37 GMT
ADD file:7c5789fb822bda2652d7addee832c5a3d71733f0f94f97d89b0c5570c0840829 in / 
# Wed, 20 Apr 2022 04:43:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:28:53 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:29:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:29:16 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:29:17 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:29:19 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:29:20 GMT
ARG GHC=9.2.2
# Wed, 20 Apr 2022 09:29:20 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 20 Apr 2022 09:30:25 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:30:32 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:30:32 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:30:36 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:30:36 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:30:36 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:85bed84afb9a834cf090b55d2e584abd55b4792d93b750db896f486680638344`  
		Last Modified: Wed, 20 Apr 2022 04:48:49 GMT  
		Size: 50.4 MB (50436985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b522b8c18adf55149c7dd6ddd4becc626f002e805952405cc9904c55e038c4c2`  
		Last Modified: Wed, 20 Apr 2022 09:38:19 GMT  
		Size: 120.6 MB (120639968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bbb5b2ebcc192a387282f0d58027a5e65da5844d39689ac323a0d7192d6e7a`  
		Last Modified: Wed, 20 Apr 2022 09:38:02 GMT  
		Size: 10.0 MB (10032282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6c2e9e6a17b4aaf841639cfb346e31ed6887458f506e32e6e407371822fbff`  
		Last Modified: Wed, 20 Apr 2022 09:39:08 GMT  
		Size: 341.0 MB (341017006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37705d98ee41cfe0ebbac02e738ee2c630b751a9f2779fa0eb22a623a0ce6406`  
		Last Modified: Wed, 20 Apr 2022 09:38:04 GMT  
		Size: 17.9 MB (17926649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.2.2-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:103a94c87cf5679f23c2477e9fd11e1f7077f1740ba71b9e8aad797f68dc0c18
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.6 MB (586552265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:356a1d587827e5f83f872cedb3bb173889426295d950a044ac5b1d1ee1357d80`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:22 GMT
ADD file:5286ff5db23c42ac6a437e8f2f9ef01b6ee6e523d7866c752428d54f177c7108 in / 
# Wed, 20 Apr 2022 04:29:22 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 08:59:16 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 08:59:36 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 08:59:37 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 08:59:37 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 08:59:41 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 08:59:41 GMT
ARG GHC=9.2.2
# Wed, 20 Apr 2022 08:59:42 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 20 Apr 2022 09:00:52 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:00:53 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:00:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:00:55 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:00:56 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:00:56 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b9f330b3a7e234282d632d95bd19a655cf0e06c1a76a51d0f73b9581be8f851b`  
		Last Modified: Wed, 20 Apr 2022 04:36:12 GMT  
		Size: 49.2 MB (49227738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5ee4bd4966ccf295d78d6280d9c6c58bb10c7101e786dad41eca501be7bc3d`  
		Last Modified: Wed, 20 Apr 2022 09:09:35 GMT  
		Size: 114.7 MB (114682952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f32f6654228ae9b68ace1b0f310037fbea0486b4256d01c705c6151d221b6e`  
		Last Modified: Wed, 20 Apr 2022 09:09:24 GMT  
		Size: 17.0 MB (16983880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71d8f04ee288260f5c56be044c8d3df485ab4d58aee98283c06b940762e12d8`  
		Last Modified: Wed, 20 Apr 2022 09:10:41 GMT  
		Size: 405.7 MB (405657695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.2.2-slim`

```console
$ docker pull haskell@sha256:7252508f81c0e0a05f93727969f44ceafa3f7188bc53bed8f44e48b4160295cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.2.2-slim` - linux; amd64

```console
$ docker pull haskell@sha256:5f15f23eeb9c2c4db14fa0e1e5d2a770a6a024114aa9e0e11d2db2a6d216ce96
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.2 MB (368220347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810fded7b58e5a381c4220c438ece5b79f93f1a069da0c233052fde981ebca31`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:30:46 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:31:05 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:31:06 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:31:06 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:31:08 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:31:09 GMT
ARG GHC=9.2.2
# Wed, 20 Apr 2022 09:31:09 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 20 Apr 2022 09:32:05 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:32:09 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:32:09 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:32:12 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:32:12 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:32:12 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2614050a0a5f46894d8232687f8437a82fe2d5becd1be0d0e86309b437e8cf`  
		Last Modified: Wed, 20 Apr 2022 09:39:55 GMT  
		Size: 94.0 MB (93994300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c71673cbdf81d2f1ac583fe12755a6ca5820194658d4f1fef0ff70568f798f`  
		Last Modified: Wed, 20 Apr 2022 09:39:43 GMT  
		Size: 10.0 MB (10032281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4203c687a2c1f84741fd0c89a57f821d6e4b3e917e2d0135e059e5f983b20b19`  
		Last Modified: Wed, 20 Apr 2022 09:40:25 GMT  
		Size: 219.1 MB (219126455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24c61b185e6c468d5348e50c481053315d6cd79b1ba16d4c9f921a0cfaa896e`  
		Last Modified: Wed, 20 Apr 2022 09:39:44 GMT  
		Size: 17.9 MB (17926647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.2.2-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:65b2614cf4553c59da1e6e89a69ec66381313f124509423d0c95d62f2b20d89c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.9 MB (391852184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025a295bdb9f1d5eff4ee739f75787e4f66d15581141a4fc6fc98ff2f4d9a683`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:36 GMT
ADD file:5de4397c1295f7249c93907be599d96efbd9cd25909340d245ec8d1c9770f444 in / 
# Wed, 20 Apr 2022 04:29:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:01:12 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:01:30 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:01:31 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:01:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:01:35 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:01:35 GMT
ARG GHC=9.2.2
# Wed, 20 Apr 2022 09:01:36 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 20 Apr 2022 09:02:41 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:02:41 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:02:42 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:02:43 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:02:44 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:02:45 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6c3e5b218d6477ff77053280968d5bdeaa5dcf16a803e917d98dd0ea8b93ac82`  
		Last Modified: Wed, 20 Apr 2022 04:36:38 GMT  
		Size: 25.9 MB (25908349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5c65fed0b5ed83432918c6a2ad9f45a492561115f67fd6a3cf95ee31e2b52f`  
		Last Modified: Wed, 20 Apr 2022 09:11:22 GMT  
		Size: 88.0 MB (88019933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5f97ca95a1b2683266801fff26205c1a3921ea8d3e1d61980edd259cc77d65`  
		Last Modified: Wed, 20 Apr 2022 09:11:13 GMT  
		Size: 17.0 MB (16983876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f9af39df7c7bb928d2f8fa1b872b53cc164f5171b1e446372248960cf3637b`  
		Last Modified: Wed, 20 Apr 2022 09:12:03 GMT  
		Size: 260.9 MB (260940026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.2.2-slim-buster`

```console
$ docker pull haskell@sha256:7252508f81c0e0a05f93727969f44ceafa3f7188bc53bed8f44e48b4160295cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.2.2-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:5f15f23eeb9c2c4db14fa0e1e5d2a770a6a024114aa9e0e11d2db2a6d216ce96
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.2 MB (368220347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810fded7b58e5a381c4220c438ece5b79f93f1a069da0c233052fde981ebca31`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:30:46 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:31:05 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:31:06 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:31:06 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:31:08 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:31:09 GMT
ARG GHC=9.2.2
# Wed, 20 Apr 2022 09:31:09 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 20 Apr 2022 09:32:05 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:32:09 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:32:09 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:32:12 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:32:12 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:32:12 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2614050a0a5f46894d8232687f8437a82fe2d5becd1be0d0e86309b437e8cf`  
		Last Modified: Wed, 20 Apr 2022 09:39:55 GMT  
		Size: 94.0 MB (93994300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c71673cbdf81d2f1ac583fe12755a6ca5820194658d4f1fef0ff70568f798f`  
		Last Modified: Wed, 20 Apr 2022 09:39:43 GMT  
		Size: 10.0 MB (10032281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4203c687a2c1f84741fd0c89a57f821d6e4b3e917e2d0135e059e5f983b20b19`  
		Last Modified: Wed, 20 Apr 2022 09:40:25 GMT  
		Size: 219.1 MB (219126455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24c61b185e6c468d5348e50c481053315d6cd79b1ba16d4c9f921a0cfaa896e`  
		Last Modified: Wed, 20 Apr 2022 09:39:44 GMT  
		Size: 17.9 MB (17926647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.2.2-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:65b2614cf4553c59da1e6e89a69ec66381313f124509423d0c95d62f2b20d89c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.9 MB (391852184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025a295bdb9f1d5eff4ee739f75787e4f66d15581141a4fc6fc98ff2f4d9a683`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:36 GMT
ADD file:5de4397c1295f7249c93907be599d96efbd9cd25909340d245ec8d1c9770f444 in / 
# Wed, 20 Apr 2022 04:29:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:01:12 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:01:30 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:01:31 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:01:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:01:35 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:01:35 GMT
ARG GHC=9.2.2
# Wed, 20 Apr 2022 09:01:36 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 20 Apr 2022 09:02:41 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:02:41 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:02:42 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:02:43 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:02:44 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:02:45 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6c3e5b218d6477ff77053280968d5bdeaa5dcf16a803e917d98dd0ea8b93ac82`  
		Last Modified: Wed, 20 Apr 2022 04:36:38 GMT  
		Size: 25.9 MB (25908349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5c65fed0b5ed83432918c6a2ad9f45a492561115f67fd6a3cf95ee31e2b52f`  
		Last Modified: Wed, 20 Apr 2022 09:11:22 GMT  
		Size: 88.0 MB (88019933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5f97ca95a1b2683266801fff26205c1a3921ea8d3e1d61980edd259cc77d65`  
		Last Modified: Wed, 20 Apr 2022 09:11:13 GMT  
		Size: 17.0 MB (16983876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f9af39df7c7bb928d2f8fa1b872b53cc164f5171b1e446372248960cf3637b`  
		Last Modified: Wed, 20 Apr 2022 09:12:03 GMT  
		Size: 260.9 MB (260940026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:buster`

```console
$ docker pull haskell@sha256:f99b7e5417f75089b53e1077a68c6333c48b82aff478a8af292a7b7f8e541832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:buster` - linux; amd64

```console
$ docker pull haskell@sha256:25cdcca5b4cf85e1ac8a73d010f260bfa65c7d4641c727253e82292e0f47fe0a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.1 MB (540052890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02fcce7eeaf2151ffd78b7a37010f74d1faaf6310e25476376964ba31822e6f2`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:37 GMT
ADD file:7c5789fb822bda2652d7addee832c5a3d71733f0f94f97d89b0c5570c0840829 in / 
# Wed, 20 Apr 2022 04:43:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:28:53 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:29:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:29:16 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:29:17 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:29:19 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:29:20 GMT
ARG GHC=9.2.2
# Wed, 20 Apr 2022 09:29:20 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 20 Apr 2022 09:30:25 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:30:32 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:30:32 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:30:36 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:30:36 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:30:36 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:85bed84afb9a834cf090b55d2e584abd55b4792d93b750db896f486680638344`  
		Last Modified: Wed, 20 Apr 2022 04:48:49 GMT  
		Size: 50.4 MB (50436985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b522b8c18adf55149c7dd6ddd4becc626f002e805952405cc9904c55e038c4c2`  
		Last Modified: Wed, 20 Apr 2022 09:38:19 GMT  
		Size: 120.6 MB (120639968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bbb5b2ebcc192a387282f0d58027a5e65da5844d39689ac323a0d7192d6e7a`  
		Last Modified: Wed, 20 Apr 2022 09:38:02 GMT  
		Size: 10.0 MB (10032282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6c2e9e6a17b4aaf841639cfb346e31ed6887458f506e32e6e407371822fbff`  
		Last Modified: Wed, 20 Apr 2022 09:39:08 GMT  
		Size: 341.0 MB (341017006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37705d98ee41cfe0ebbac02e738ee2c630b751a9f2779fa0eb22a623a0ce6406`  
		Last Modified: Wed, 20 Apr 2022 09:38:04 GMT  
		Size: 17.9 MB (17926649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:103a94c87cf5679f23c2477e9fd11e1f7077f1740ba71b9e8aad797f68dc0c18
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.6 MB (586552265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:356a1d587827e5f83f872cedb3bb173889426295d950a044ac5b1d1ee1357d80`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:22 GMT
ADD file:5286ff5db23c42ac6a437e8f2f9ef01b6ee6e523d7866c752428d54f177c7108 in / 
# Wed, 20 Apr 2022 04:29:22 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 08:59:16 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 08:59:36 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 08:59:37 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 08:59:37 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 08:59:41 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 08:59:41 GMT
ARG GHC=9.2.2
# Wed, 20 Apr 2022 08:59:42 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 20 Apr 2022 09:00:52 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:00:53 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:00:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:00:55 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:00:56 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:00:56 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b9f330b3a7e234282d632d95bd19a655cf0e06c1a76a51d0f73b9581be8f851b`  
		Last Modified: Wed, 20 Apr 2022 04:36:12 GMT  
		Size: 49.2 MB (49227738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5ee4bd4966ccf295d78d6280d9c6c58bb10c7101e786dad41eca501be7bc3d`  
		Last Modified: Wed, 20 Apr 2022 09:09:35 GMT  
		Size: 114.7 MB (114682952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f32f6654228ae9b68ace1b0f310037fbea0486b4256d01c705c6151d221b6e`  
		Last Modified: Wed, 20 Apr 2022 09:09:24 GMT  
		Size: 17.0 MB (16983880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71d8f04ee288260f5c56be044c8d3df485ab4d58aee98283c06b940762e12d8`  
		Last Modified: Wed, 20 Apr 2022 09:10:41 GMT  
		Size: 405.7 MB (405657695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:latest`

```console
$ docker pull haskell@sha256:f99b7e5417f75089b53e1077a68c6333c48b82aff478a8af292a7b7f8e541832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:latest` - linux; amd64

```console
$ docker pull haskell@sha256:25cdcca5b4cf85e1ac8a73d010f260bfa65c7d4641c727253e82292e0f47fe0a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.1 MB (540052890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02fcce7eeaf2151ffd78b7a37010f74d1faaf6310e25476376964ba31822e6f2`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:37 GMT
ADD file:7c5789fb822bda2652d7addee832c5a3d71733f0f94f97d89b0c5570c0840829 in / 
# Wed, 20 Apr 2022 04:43:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:28:53 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:29:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:29:16 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:29:17 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:29:19 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:29:20 GMT
ARG GHC=9.2.2
# Wed, 20 Apr 2022 09:29:20 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 20 Apr 2022 09:30:25 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:30:32 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:30:32 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:30:36 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:30:36 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:30:36 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:85bed84afb9a834cf090b55d2e584abd55b4792d93b750db896f486680638344`  
		Last Modified: Wed, 20 Apr 2022 04:48:49 GMT  
		Size: 50.4 MB (50436985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b522b8c18adf55149c7dd6ddd4becc626f002e805952405cc9904c55e038c4c2`  
		Last Modified: Wed, 20 Apr 2022 09:38:19 GMT  
		Size: 120.6 MB (120639968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bbb5b2ebcc192a387282f0d58027a5e65da5844d39689ac323a0d7192d6e7a`  
		Last Modified: Wed, 20 Apr 2022 09:38:02 GMT  
		Size: 10.0 MB (10032282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6c2e9e6a17b4aaf841639cfb346e31ed6887458f506e32e6e407371822fbff`  
		Last Modified: Wed, 20 Apr 2022 09:39:08 GMT  
		Size: 341.0 MB (341017006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37705d98ee41cfe0ebbac02e738ee2c630b751a9f2779fa0eb22a623a0ce6406`  
		Last Modified: Wed, 20 Apr 2022 09:38:04 GMT  
		Size: 17.9 MB (17926649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:latest` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:103a94c87cf5679f23c2477e9fd11e1f7077f1740ba71b9e8aad797f68dc0c18
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.6 MB (586552265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:356a1d587827e5f83f872cedb3bb173889426295d950a044ac5b1d1ee1357d80`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:22 GMT
ADD file:5286ff5db23c42ac6a437e8f2f9ef01b6ee6e523d7866c752428d54f177c7108 in / 
# Wed, 20 Apr 2022 04:29:22 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 08:59:16 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 08:59:36 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 08:59:37 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 08:59:37 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 08:59:41 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 08:59:41 GMT
ARG GHC=9.2.2
# Wed, 20 Apr 2022 08:59:42 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 20 Apr 2022 09:00:52 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:00:53 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:00:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:00:55 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:00:56 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:00:56 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b9f330b3a7e234282d632d95bd19a655cf0e06c1a76a51d0f73b9581be8f851b`  
		Last Modified: Wed, 20 Apr 2022 04:36:12 GMT  
		Size: 49.2 MB (49227738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5ee4bd4966ccf295d78d6280d9c6c58bb10c7101e786dad41eca501be7bc3d`  
		Last Modified: Wed, 20 Apr 2022 09:09:35 GMT  
		Size: 114.7 MB (114682952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f32f6654228ae9b68ace1b0f310037fbea0486b4256d01c705c6151d221b6e`  
		Last Modified: Wed, 20 Apr 2022 09:09:24 GMT  
		Size: 17.0 MB (16983880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71d8f04ee288260f5c56be044c8d3df485ab4d58aee98283c06b940762e12d8`  
		Last Modified: Wed, 20 Apr 2022 09:10:41 GMT  
		Size: 405.7 MB (405657695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:slim`

```console
$ docker pull haskell@sha256:7252508f81c0e0a05f93727969f44ceafa3f7188bc53bed8f44e48b4160295cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:slim` - linux; amd64

```console
$ docker pull haskell@sha256:5f15f23eeb9c2c4db14fa0e1e5d2a770a6a024114aa9e0e11d2db2a6d216ce96
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.2 MB (368220347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810fded7b58e5a381c4220c438ece5b79f93f1a069da0c233052fde981ebca31`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:30:46 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:31:05 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:31:06 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:31:06 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:31:08 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:31:09 GMT
ARG GHC=9.2.2
# Wed, 20 Apr 2022 09:31:09 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 20 Apr 2022 09:32:05 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:32:09 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:32:09 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:32:12 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:32:12 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:32:12 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2614050a0a5f46894d8232687f8437a82fe2d5becd1be0d0e86309b437e8cf`  
		Last Modified: Wed, 20 Apr 2022 09:39:55 GMT  
		Size: 94.0 MB (93994300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c71673cbdf81d2f1ac583fe12755a6ca5820194658d4f1fef0ff70568f798f`  
		Last Modified: Wed, 20 Apr 2022 09:39:43 GMT  
		Size: 10.0 MB (10032281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4203c687a2c1f84741fd0c89a57f821d6e4b3e917e2d0135e059e5f983b20b19`  
		Last Modified: Wed, 20 Apr 2022 09:40:25 GMT  
		Size: 219.1 MB (219126455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24c61b185e6c468d5348e50c481053315d6cd79b1ba16d4c9f921a0cfaa896e`  
		Last Modified: Wed, 20 Apr 2022 09:39:44 GMT  
		Size: 17.9 MB (17926647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:65b2614cf4553c59da1e6e89a69ec66381313f124509423d0c95d62f2b20d89c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.9 MB (391852184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025a295bdb9f1d5eff4ee739f75787e4f66d15581141a4fc6fc98ff2f4d9a683`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:36 GMT
ADD file:5de4397c1295f7249c93907be599d96efbd9cd25909340d245ec8d1c9770f444 in / 
# Wed, 20 Apr 2022 04:29:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:01:12 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:01:30 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:01:31 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:01:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:01:35 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:01:35 GMT
ARG GHC=9.2.2
# Wed, 20 Apr 2022 09:01:36 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 20 Apr 2022 09:02:41 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:02:41 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:02:42 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:02:43 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:02:44 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:02:45 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6c3e5b218d6477ff77053280968d5bdeaa5dcf16a803e917d98dd0ea8b93ac82`  
		Last Modified: Wed, 20 Apr 2022 04:36:38 GMT  
		Size: 25.9 MB (25908349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5c65fed0b5ed83432918c6a2ad9f45a492561115f67fd6a3cf95ee31e2b52f`  
		Last Modified: Wed, 20 Apr 2022 09:11:22 GMT  
		Size: 88.0 MB (88019933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5f97ca95a1b2683266801fff26205c1a3921ea8d3e1d61980edd259cc77d65`  
		Last Modified: Wed, 20 Apr 2022 09:11:13 GMT  
		Size: 17.0 MB (16983876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f9af39df7c7bb928d2f8fa1b872b53cc164f5171b1e446372248960cf3637b`  
		Last Modified: Wed, 20 Apr 2022 09:12:03 GMT  
		Size: 260.9 MB (260940026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:slim-buster`

```console
$ docker pull haskell@sha256:7252508f81c0e0a05f93727969f44ceafa3f7188bc53bed8f44e48b4160295cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:5f15f23eeb9c2c4db14fa0e1e5d2a770a6a024114aa9e0e11d2db2a6d216ce96
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.2 MB (368220347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810fded7b58e5a381c4220c438ece5b79f93f1a069da0c233052fde981ebca31`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:30:46 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:31:05 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:31:06 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:31:06 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:31:08 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:31:09 GMT
ARG GHC=9.2.2
# Wed, 20 Apr 2022 09:31:09 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 20 Apr 2022 09:32:05 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:32:09 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:32:09 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:32:12 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:32:12 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:32:12 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2614050a0a5f46894d8232687f8437a82fe2d5becd1be0d0e86309b437e8cf`  
		Last Modified: Wed, 20 Apr 2022 09:39:55 GMT  
		Size: 94.0 MB (93994300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c71673cbdf81d2f1ac583fe12755a6ca5820194658d4f1fef0ff70568f798f`  
		Last Modified: Wed, 20 Apr 2022 09:39:43 GMT  
		Size: 10.0 MB (10032281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4203c687a2c1f84741fd0c89a57f821d6e4b3e917e2d0135e059e5f983b20b19`  
		Last Modified: Wed, 20 Apr 2022 09:40:25 GMT  
		Size: 219.1 MB (219126455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24c61b185e6c468d5348e50c481053315d6cd79b1ba16d4c9f921a0cfaa896e`  
		Last Modified: Wed, 20 Apr 2022 09:39:44 GMT  
		Size: 17.9 MB (17926647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:65b2614cf4553c59da1e6e89a69ec66381313f124509423d0c95d62f2b20d89c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.9 MB (391852184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025a295bdb9f1d5eff4ee739f75787e4f66d15581141a4fc6fc98ff2f4d9a683`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 20 Apr 2022 04:29:36 GMT
ADD file:5de4397c1295f7249c93907be599d96efbd9cd25909340d245ec8d1c9770f444 in / 
# Wed, 20 Apr 2022 04:29:37 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 09:01:12 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 09:01:30 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 09:01:31 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 20 Apr 2022 09:01:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 20 Apr 2022 09:01:35 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 20 Apr 2022 09:01:35 GMT
ARG GHC=9.2.2
# Wed, 20 Apr 2022 09:01:36 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 20 Apr 2022 09:02:41 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 20 Apr 2022 09:02:41 GMT
ARG STACK=2.7.5
# Wed, 20 Apr 2022 09:02:42 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 20 Apr 2022 09:02:43 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 20 Apr 2022 09:02:44 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 09:02:45 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6c3e5b218d6477ff77053280968d5bdeaa5dcf16a803e917d98dd0ea8b93ac82`  
		Last Modified: Wed, 20 Apr 2022 04:36:38 GMT  
		Size: 25.9 MB (25908349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5c65fed0b5ed83432918c6a2ad9f45a492561115f67fd6a3cf95ee31e2b52f`  
		Last Modified: Wed, 20 Apr 2022 09:11:22 GMT  
		Size: 88.0 MB (88019933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5f97ca95a1b2683266801fff26205c1a3921ea8d3e1d61980edd259cc77d65`  
		Last Modified: Wed, 20 Apr 2022 09:11:13 GMT  
		Size: 17.0 MB (16983876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f9af39df7c7bb928d2f8fa1b872b53cc164f5171b1e446372248960cf3637b`  
		Last Modified: Wed, 20 Apr 2022 09:12:03 GMT  
		Size: 260.9 MB (260940026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
