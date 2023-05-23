<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `haskell`

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
-	[`haskell:9.2.7`](#haskell927)
-	[`haskell:9.2.7-buster`](#haskell927-buster)
-	[`haskell:9.2.7-slim`](#haskell927-slim)
-	[`haskell:9.2.7-slim-buster`](#haskell927-slim-buster)
-	[`haskell:9.4`](#haskell94)
-	[`haskell:9.4-buster`](#haskell94-buster)
-	[`haskell:9.4-slim`](#haskell94-slim)
-	[`haskell:9.4-slim-buster`](#haskell94-slim-buster)
-	[`haskell:9.4.5`](#haskell945)
-	[`haskell:9.4.5-buster`](#haskell945-buster)
-	[`haskell:9.4.5-slim`](#haskell945-slim)
-	[`haskell:9.4.5-slim-buster`](#haskell945-slim-buster)
-	[`haskell:buster`](#haskellbuster)
-	[`haskell:latest`](#haskelllatest)
-	[`haskell:slim`](#haskellslim)
-	[`haskell:slim-buster`](#haskellslim-buster)

## `haskell:9`

```console
$ docker pull haskell@sha256:061a6d9588fc9fef00dc758428ee80db3e3d5c0b0b85666adefced246b7ab093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9` - linux; amd64

```console
$ docker pull haskell@sha256:e8609d28576e5715376ac4e4d12bc1a1680807c003e9b2f11b06a1c94312d193
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **721.3 MB (721262460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e0874f8537eeb3b079a734c33eafbf8ec0254c88e3e219bed678290e5d66d4`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 01:20:24 GMT
ADD file:9d769df745075dbc4cd2c01ca784571a0df008f6b650b895a7f92d3281132807 in / 
# Tue, 23 May 2023 01:20:25 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:50:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:50:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:52:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:25:03 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 08:25:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:25:08 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 08:25:08 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 08:25:11 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 08:25:11 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 08:25:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 08:25:14 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 08:25:14 GMT
ARG GHC=9.4.5
# Tue, 23 May 2023 08:25:14 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Tue, 23 May 2023 08:26:36 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.5 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='ecf16ec503e739e727174b29e5acbe4cf0c54737dd4d5eda046e09323f9ee248';             ;;         'x86_64')             GHC_SHA256='a44c39c4cc9a147de6dd31762995a9e47467cc91757800d80667b8cd60a9b226';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 08:26:43 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.5/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:26:43 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c722db24a050621ee87ea07acd5d066d3d6a94737c32012f27d73a1ad5cc645c`  
		Last Modified: Tue, 23 May 2023 01:24:26 GMT  
		Size: 50.4 MB (50448716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f8e4a0ed530ff1c74aea38be7ec6c725334c7c3a551b417d0f6f9e220a36fb`  
		Last Modified: Tue, 23 May 2023 01:57:08 GMT  
		Size: 17.6 MB (17580817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a739c67a76c3ff201aa979efc9c5deb081a75f5b98390ee176315cb0cb582aa9`  
		Last Modified: Tue, 23 May 2023 01:57:23 GMT  
		Size: 51.9 MB (51878369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e0d706266f768c6ed028e990dbb063fc43f6028827fe0f39ee6539a963e677`  
		Last Modified: Tue, 23 May 2023 01:57:52 GMT  
		Size: 191.9 MB (191886143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5899d9687951ca93548ece5e39287dc4f5b87d6733a2329490b95ac49b475905`  
		Last Modified: Tue, 23 May 2023 08:34:40 GMT  
		Size: 514.8 KB (514774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729ae0213f5e911798d1f7c2f3be7eaabda44bbf485853229978e6ea41918170`  
		Last Modified: Tue, 23 May 2023 08:34:42 GMT  
		Size: 13.7 MB (13736490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a49eb74c9b4a45e0eaf2f542af477fb0878c8110e8d36e175cb279b0e281636`  
		Last Modified: Tue, 23 May 2023 08:34:42 GMT  
		Size: 7.8 MB (7838367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55634913539c42cfcf42734839420cfb08b31a3ba2d1a174dd88894b1114e064`  
		Last Modified: Tue, 23 May 2023 08:35:46 GMT  
		Size: 387.4 MB (387378784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:c6ff674da0b5d75136bfad35ca6be581c583586625b0fc36f0a256ce0241ed62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **766.2 MB (766222838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77be8ca114cff75846de2efa9954abf091d4d3ac07a82c7d642595fa3f598b8`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 03 May 2023 00:22:56 GMT
ADD file:6042e29dcf5e22439cd69873d8960f8d3977abe915ef462aaa84368a7186a3bf in / 
# Wed, 03 May 2023 00:22:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:22:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:23:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:24:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 06:50:35 GMT
ENV LANG=C.UTF-8
# Thu, 04 May 2023 06:50:38 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 06:50:38 GMT
ARG STACK=2.9.3
# Thu, 04 May 2023 06:50:38 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 04 May 2023 06:50:42 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 04 May 2023 06:50:42 GMT
ARG CABAL_INSTALL=3.8.1.0
# Thu, 04 May 2023 06:50:42 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Thu, 04 May 2023 06:50:44 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 04 May 2023 06:50:44 GMT
ARG GHC=9.4.5
# Thu, 04 May 2023 06:50:44 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Thu, 04 May 2023 06:52:02 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.5 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='ecf16ec503e739e727174b29e5acbe4cf0c54737dd4d5eda046e09323f9ee248';             ;;         'x86_64')             GHC_SHA256='a44c39c4cc9a147de6dd31762995a9e47467cc91757800d80667b8cd60a9b226';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 04 May 2023 06:52:18 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.5/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 06:52:18 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b7c5fe8e0ac53c77142bf16686fc01d0d2b1fb2da7be5414cdf2f224ec485592`  
		Last Modified: Wed, 03 May 2023 00:26:10 GMT  
		Size: 49.2 MB (49238630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced623c8f9593ccbdc26a5e9ad9d9ad18aa6a8a3b82d7db591552673ac8e3281`  
		Last Modified: Wed, 03 May 2023 17:37:59 GMT  
		Size: 17.5 MB (17450341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fc649f7c89c148c32767dadfc283ae1472705773920b21ddd2bc77d49b2d64`  
		Last Modified: Wed, 03 May 2023 17:38:14 GMT  
		Size: 52.2 MB (52190435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7089b0cf38b0c4474188c7904744a3a55656697b95a3b5088cb510d0e932ba7`  
		Last Modified: Wed, 03 May 2023 17:38:38 GMT  
		Size: 183.5 MB (183454524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b29e6814a3ae5bdbc407544a41b3a6e63f55f582feff0b958bd39a45cac7ea`  
		Last Modified: Thu, 04 May 2023 06:55:45 GMT  
		Size: 517.0 KB (516952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a74f7761e2befcf0d84ef09bdf0daa0a7d4789a63da4f0384d3dc6a7246f1cc`  
		Last Modified: Thu, 04 May 2023 06:55:47 GMT  
		Size: 15.4 MB (15374096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108ebc522e506a00d8bd87318b5a587329490286725a8267770ee95b0caf2273`  
		Last Modified: Thu, 04 May 2023 06:55:47 GMT  
		Size: 12.4 MB (12373196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff3ed3db5bee2805f9b104d9e3c2ce074ec04bdd666c74d543802081ed6c5f6`  
		Last Modified: Thu, 04 May 2023 06:56:48 GMT  
		Size: 435.6 MB (435624664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9-buster`

```console
$ docker pull haskell@sha256:061a6d9588fc9fef00dc758428ee80db3e3d5c0b0b85666adefced246b7ab093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9-buster` - linux; amd64

```console
$ docker pull haskell@sha256:e8609d28576e5715376ac4e4d12bc1a1680807c003e9b2f11b06a1c94312d193
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **721.3 MB (721262460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e0874f8537eeb3b079a734c33eafbf8ec0254c88e3e219bed678290e5d66d4`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 01:20:24 GMT
ADD file:9d769df745075dbc4cd2c01ca784571a0df008f6b650b895a7f92d3281132807 in / 
# Tue, 23 May 2023 01:20:25 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:50:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:50:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:52:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:25:03 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 08:25:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:25:08 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 08:25:08 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 08:25:11 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 08:25:11 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 08:25:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 08:25:14 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 08:25:14 GMT
ARG GHC=9.4.5
# Tue, 23 May 2023 08:25:14 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Tue, 23 May 2023 08:26:36 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.5 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='ecf16ec503e739e727174b29e5acbe4cf0c54737dd4d5eda046e09323f9ee248';             ;;         'x86_64')             GHC_SHA256='a44c39c4cc9a147de6dd31762995a9e47467cc91757800d80667b8cd60a9b226';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 08:26:43 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.5/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:26:43 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c722db24a050621ee87ea07acd5d066d3d6a94737c32012f27d73a1ad5cc645c`  
		Last Modified: Tue, 23 May 2023 01:24:26 GMT  
		Size: 50.4 MB (50448716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f8e4a0ed530ff1c74aea38be7ec6c725334c7c3a551b417d0f6f9e220a36fb`  
		Last Modified: Tue, 23 May 2023 01:57:08 GMT  
		Size: 17.6 MB (17580817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a739c67a76c3ff201aa979efc9c5deb081a75f5b98390ee176315cb0cb582aa9`  
		Last Modified: Tue, 23 May 2023 01:57:23 GMT  
		Size: 51.9 MB (51878369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e0d706266f768c6ed028e990dbb063fc43f6028827fe0f39ee6539a963e677`  
		Last Modified: Tue, 23 May 2023 01:57:52 GMT  
		Size: 191.9 MB (191886143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5899d9687951ca93548ece5e39287dc4f5b87d6733a2329490b95ac49b475905`  
		Last Modified: Tue, 23 May 2023 08:34:40 GMT  
		Size: 514.8 KB (514774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729ae0213f5e911798d1f7c2f3be7eaabda44bbf485853229978e6ea41918170`  
		Last Modified: Tue, 23 May 2023 08:34:42 GMT  
		Size: 13.7 MB (13736490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a49eb74c9b4a45e0eaf2f542af477fb0878c8110e8d36e175cb279b0e281636`  
		Last Modified: Tue, 23 May 2023 08:34:42 GMT  
		Size: 7.8 MB (7838367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55634913539c42cfcf42734839420cfb08b31a3ba2d1a174dd88894b1114e064`  
		Last Modified: Tue, 23 May 2023 08:35:46 GMT  
		Size: 387.4 MB (387378784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:c6ff674da0b5d75136bfad35ca6be581c583586625b0fc36f0a256ce0241ed62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **766.2 MB (766222838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77be8ca114cff75846de2efa9954abf091d4d3ac07a82c7d642595fa3f598b8`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 03 May 2023 00:22:56 GMT
ADD file:6042e29dcf5e22439cd69873d8960f8d3977abe915ef462aaa84368a7186a3bf in / 
# Wed, 03 May 2023 00:22:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:22:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:23:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:24:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 06:50:35 GMT
ENV LANG=C.UTF-8
# Thu, 04 May 2023 06:50:38 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 06:50:38 GMT
ARG STACK=2.9.3
# Thu, 04 May 2023 06:50:38 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 04 May 2023 06:50:42 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 04 May 2023 06:50:42 GMT
ARG CABAL_INSTALL=3.8.1.0
# Thu, 04 May 2023 06:50:42 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Thu, 04 May 2023 06:50:44 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 04 May 2023 06:50:44 GMT
ARG GHC=9.4.5
# Thu, 04 May 2023 06:50:44 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Thu, 04 May 2023 06:52:02 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.5 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='ecf16ec503e739e727174b29e5acbe4cf0c54737dd4d5eda046e09323f9ee248';             ;;         'x86_64')             GHC_SHA256='a44c39c4cc9a147de6dd31762995a9e47467cc91757800d80667b8cd60a9b226';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 04 May 2023 06:52:18 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.5/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 06:52:18 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b7c5fe8e0ac53c77142bf16686fc01d0d2b1fb2da7be5414cdf2f224ec485592`  
		Last Modified: Wed, 03 May 2023 00:26:10 GMT  
		Size: 49.2 MB (49238630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced623c8f9593ccbdc26a5e9ad9d9ad18aa6a8a3b82d7db591552673ac8e3281`  
		Last Modified: Wed, 03 May 2023 17:37:59 GMT  
		Size: 17.5 MB (17450341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fc649f7c89c148c32767dadfc283ae1472705773920b21ddd2bc77d49b2d64`  
		Last Modified: Wed, 03 May 2023 17:38:14 GMT  
		Size: 52.2 MB (52190435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7089b0cf38b0c4474188c7904744a3a55656697b95a3b5088cb510d0e932ba7`  
		Last Modified: Wed, 03 May 2023 17:38:38 GMT  
		Size: 183.5 MB (183454524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b29e6814a3ae5bdbc407544a41b3a6e63f55f582feff0b958bd39a45cac7ea`  
		Last Modified: Thu, 04 May 2023 06:55:45 GMT  
		Size: 517.0 KB (516952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a74f7761e2befcf0d84ef09bdf0daa0a7d4789a63da4f0384d3dc6a7246f1cc`  
		Last Modified: Thu, 04 May 2023 06:55:47 GMT  
		Size: 15.4 MB (15374096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108ebc522e506a00d8bd87318b5a587329490286725a8267770ee95b0caf2273`  
		Last Modified: Thu, 04 May 2023 06:55:47 GMT  
		Size: 12.4 MB (12373196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff3ed3db5bee2805f9b104d9e3c2ce074ec04bdd666c74d543802081ed6c5f6`  
		Last Modified: Thu, 04 May 2023 06:56:48 GMT  
		Size: 435.6 MB (435624664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9-slim`

```console
$ docker pull haskell@sha256:77551349dce35ba3f6f95ad53d736e261ab59b467a3af4164b5bfa51ccebfcce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9-slim` - linux; amd64

```console
$ docker pull haskell@sha256:89fb63973f87062b26c1cab096f57c5b22b59473ba47f66389ad7ca078e706f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.0 MB (412025721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd594b4728b6f2ba7bb38f2fb399469ef9007208631c554c3e8f71b6f4eda081`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 01:20:37 GMT
ADD file:2058e04b33179527a56999678c1c62dfcf76944675afcd77b5163141fb025f8c in / 
# Tue, 23 May 2023 01:20:37 GMT
CMD ["bash"]
# Tue, 23 May 2023 08:26:56 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 08:27:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:27:21 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 08:27:21 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 08:27:24 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 08:27:24 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 08:27:24 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 08:27:27 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 08:27:27 GMT
ARG GHC=9.4.5
# Tue, 23 May 2023 08:27:27 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Tue, 23 May 2023 08:28:42 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.5 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='ecf16ec503e739e727174b29e5acbe4cf0c54737dd4d5eda046e09323f9ee248';             ;;         'x86_64')             GHC_SHA256='a44c39c4cc9a147de6dd31762995a9e47467cc91757800d80667b8cd60a9b226';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 08:28:47 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.5/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:28:47 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:99bf4787315b60d97d860ac6d006b7835b2241a601e93c2da4af6ca554be8704`  
		Last Modified: Tue, 23 May 2023 01:24:47 GMT  
		Size: 27.1 MB (27138577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922ab778f24e7006dd142f8df643984e8c1e678939e7104343f0975f2af889aa`  
		Last Modified: Tue, 23 May 2023 08:36:22 GMT  
		Size: 94.0 MB (94041102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af63a62ebad853e3687cdc43c53fa1acba67c351116e01715a614573acb3b5e`  
		Last Modified: Tue, 23 May 2023 08:36:11 GMT  
		Size: 13.7 MB (13736479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd32594f8ad3cb46719679dc1bec1d16f0fbd03b2fd29976b3b1c386f6e380f`  
		Last Modified: Tue, 23 May 2023 08:36:11 GMT  
		Size: 7.8 MB (7838380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7690bb755e90f1ef3becc286ac59274aaff9dd6ecf746fad997a95d14a3520b8`  
		Last Modified: Tue, 23 May 2023 08:36:54 GMT  
		Size: 269.3 MB (269271183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:99eb1374829355eb12431ea07110fa811c4f10a051b5ba43fbfe0eb574f296be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.5 MB (434516775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bbd3cd28aaae40586bf0407842546b69b3f5cc35e0ec70393550258dc83be95`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 00:43:28 GMT
ADD file:55a469039df0bf0e94ef7cd2d6fd355ad0c69e0e23e7921194445dd1fe281e3b in / 
# Tue, 23 May 2023 00:43:28 GMT
CMD ["bash"]
# Tue, 23 May 2023 02:13:23 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 02:13:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 02:13:42 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 02:13:42 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 02:13:50 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 02:13:51 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 02:13:51 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 02:13:53 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 02:13:53 GMT
ARG GHC=9.4.5
# Tue, 23 May 2023 02:13:53 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Tue, 23 May 2023 02:15:10 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.5 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='ecf16ec503e739e727174b29e5acbe4cf0c54737dd4d5eda046e09323f9ee248';             ;;         'x86_64')             GHC_SHA256='a44c39c4cc9a147de6dd31762995a9e47467cc91757800d80667b8cd60a9b226';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 02:15:22 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.5/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 02:15:22 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:3ca7b6c7180eac66b9c4301084a16319f41eb7f7365bdf91bcc272bd24cb4149`  
		Last Modified: Tue, 23 May 2023 00:46:44 GMT  
		Size: 25.9 MB (25921744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b1dfa9c7df4de9ed05420bd02fcbf79647f01f988f262f07cb0e1e6d68323d`  
		Last Modified: Tue, 23 May 2023 02:18:44 GMT  
		Size: 88.1 MB (88056276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87343452a5afdee6a1c296325e9b85c3424d00f396673e20fcab8554166166fe`  
		Last Modified: Tue, 23 May 2023 02:18:37 GMT  
		Size: 15.4 MB (15374105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba905b5698eb25fddd7444908f68d9b3bbe45263861f4c5346d9d95da1269fde`  
		Last Modified: Tue, 23 May 2023 02:18:37 GMT  
		Size: 12.4 MB (12373178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ff7a6c59b9c4ebd1c4fe70ce63a4eb0eaa932fa606622bf1fb0a68e6be1ea5`  
		Last Modified: Tue, 23 May 2023 02:19:15 GMT  
		Size: 292.8 MB (292791472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9-slim-buster`

```console
$ docker pull haskell@sha256:77551349dce35ba3f6f95ad53d736e261ab59b467a3af4164b5bfa51ccebfcce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:89fb63973f87062b26c1cab096f57c5b22b59473ba47f66389ad7ca078e706f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.0 MB (412025721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd594b4728b6f2ba7bb38f2fb399469ef9007208631c554c3e8f71b6f4eda081`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 01:20:37 GMT
ADD file:2058e04b33179527a56999678c1c62dfcf76944675afcd77b5163141fb025f8c in / 
# Tue, 23 May 2023 01:20:37 GMT
CMD ["bash"]
# Tue, 23 May 2023 08:26:56 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 08:27:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:27:21 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 08:27:21 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 08:27:24 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 08:27:24 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 08:27:24 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 08:27:27 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 08:27:27 GMT
ARG GHC=9.4.5
# Tue, 23 May 2023 08:27:27 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Tue, 23 May 2023 08:28:42 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.5 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='ecf16ec503e739e727174b29e5acbe4cf0c54737dd4d5eda046e09323f9ee248';             ;;         'x86_64')             GHC_SHA256='a44c39c4cc9a147de6dd31762995a9e47467cc91757800d80667b8cd60a9b226';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 08:28:47 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.5/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:28:47 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:99bf4787315b60d97d860ac6d006b7835b2241a601e93c2da4af6ca554be8704`  
		Last Modified: Tue, 23 May 2023 01:24:47 GMT  
		Size: 27.1 MB (27138577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922ab778f24e7006dd142f8df643984e8c1e678939e7104343f0975f2af889aa`  
		Last Modified: Tue, 23 May 2023 08:36:22 GMT  
		Size: 94.0 MB (94041102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af63a62ebad853e3687cdc43c53fa1acba67c351116e01715a614573acb3b5e`  
		Last Modified: Tue, 23 May 2023 08:36:11 GMT  
		Size: 13.7 MB (13736479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd32594f8ad3cb46719679dc1bec1d16f0fbd03b2fd29976b3b1c386f6e380f`  
		Last Modified: Tue, 23 May 2023 08:36:11 GMT  
		Size: 7.8 MB (7838380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7690bb755e90f1ef3becc286ac59274aaff9dd6ecf746fad997a95d14a3520b8`  
		Last Modified: Tue, 23 May 2023 08:36:54 GMT  
		Size: 269.3 MB (269271183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:99eb1374829355eb12431ea07110fa811c4f10a051b5ba43fbfe0eb574f296be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.5 MB (434516775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bbd3cd28aaae40586bf0407842546b69b3f5cc35e0ec70393550258dc83be95`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 00:43:28 GMT
ADD file:55a469039df0bf0e94ef7cd2d6fd355ad0c69e0e23e7921194445dd1fe281e3b in / 
# Tue, 23 May 2023 00:43:28 GMT
CMD ["bash"]
# Tue, 23 May 2023 02:13:23 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 02:13:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 02:13:42 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 02:13:42 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 02:13:50 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 02:13:51 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 02:13:51 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 02:13:53 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 02:13:53 GMT
ARG GHC=9.4.5
# Tue, 23 May 2023 02:13:53 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Tue, 23 May 2023 02:15:10 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.5 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='ecf16ec503e739e727174b29e5acbe4cf0c54737dd4d5eda046e09323f9ee248';             ;;         'x86_64')             GHC_SHA256='a44c39c4cc9a147de6dd31762995a9e47467cc91757800d80667b8cd60a9b226';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 02:15:22 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.5/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 02:15:22 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:3ca7b6c7180eac66b9c4301084a16319f41eb7f7365bdf91bcc272bd24cb4149`  
		Last Modified: Tue, 23 May 2023 00:46:44 GMT  
		Size: 25.9 MB (25921744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b1dfa9c7df4de9ed05420bd02fcbf79647f01f988f262f07cb0e1e6d68323d`  
		Last Modified: Tue, 23 May 2023 02:18:44 GMT  
		Size: 88.1 MB (88056276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87343452a5afdee6a1c296325e9b85c3424d00f396673e20fcab8554166166fe`  
		Last Modified: Tue, 23 May 2023 02:18:37 GMT  
		Size: 15.4 MB (15374105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba905b5698eb25fddd7444908f68d9b3bbe45263861f4c5346d9d95da1269fde`  
		Last Modified: Tue, 23 May 2023 02:18:37 GMT  
		Size: 12.4 MB (12373178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ff7a6c59b9c4ebd1c4fe70ce63a4eb0eaa932fa606622bf1fb0a68e6be1ea5`  
		Last Modified: Tue, 23 May 2023 02:19:15 GMT  
		Size: 292.8 MB (292791472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0`

```console
$ docker pull haskell@sha256:798f61d841d1248e51f2a7ef1987d81ac15ffad66fa26734616ab3c3ba3a32d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.0` - linux; amd64

```console
$ docker pull haskell@sha256:bfcfbf5ff336af8bb39b5aa10ba6835ee573dd6fb0e95883588f5ec5e603b0cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **715.4 MB (715437166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ac168ad58549acac147b10b723a69ea0c57645dde84dc0ceba5285f690e2c8`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 01:20:24 GMT
ADD file:9d769df745075dbc4cd2c01ca784571a0df008f6b650b895a7f92d3281132807 in / 
# Tue, 23 May 2023 01:20:25 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:50:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:50:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:52:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:25:03 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 08:25:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:25:08 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 08:25:08 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 08:25:11 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 08:25:11 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 08:25:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 08:25:14 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 08:31:36 GMT
ARG LLVM_VERSION=12
# Tue, 23 May 2023 08:31:36 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 23 May 2023 08:31:36 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 23 May 2023 08:31:36 GMT
ARG GHC=9.0.2
# Tue, 23 May 2023 08:31:37 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 23 May 2023 08:32:48 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 08:32:55 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:32:55 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c722db24a050621ee87ea07acd5d066d3d6a94737c32012f27d73a1ad5cc645c`  
		Last Modified: Tue, 23 May 2023 01:24:26 GMT  
		Size: 50.4 MB (50448716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f8e4a0ed530ff1c74aea38be7ec6c725334c7c3a551b417d0f6f9e220a36fb`  
		Last Modified: Tue, 23 May 2023 01:57:08 GMT  
		Size: 17.6 MB (17580817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a739c67a76c3ff201aa979efc9c5deb081a75f5b98390ee176315cb0cb582aa9`  
		Last Modified: Tue, 23 May 2023 01:57:23 GMT  
		Size: 51.9 MB (51878369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e0d706266f768c6ed028e990dbb063fc43f6028827fe0f39ee6539a963e677`  
		Last Modified: Tue, 23 May 2023 01:57:52 GMT  
		Size: 191.9 MB (191886143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5899d9687951ca93548ece5e39287dc4f5b87d6733a2329490b95ac49b475905`  
		Last Modified: Tue, 23 May 2023 08:34:40 GMT  
		Size: 514.8 KB (514774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729ae0213f5e911798d1f7c2f3be7eaabda44bbf485853229978e6ea41918170`  
		Last Modified: Tue, 23 May 2023 08:34:42 GMT  
		Size: 13.7 MB (13736490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a49eb74c9b4a45e0eaf2f542af477fb0878c8110e8d36e175cb279b0e281636`  
		Last Modified: Tue, 23 May 2023 08:34:42 GMT  
		Size: 7.8 MB (7838367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2635f8f29501aeebff447b4f28162e20c221e95ff6dfe1f2063443c358304d4`  
		Last Modified: Tue, 23 May 2023 08:40:59 GMT  
		Size: 381.6 MB (381553490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.0` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:cf6d9062b0546e88dc415d31385a7c9976a5221182fb508648eb2e1a3635443e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.8 MB (639805195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b9ed0f7adcc993d721155cd76ca0528e1a56d340a3be76a0e28209d2912fe8`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 03 May 2023 00:22:56 GMT
ADD file:6042e29dcf5e22439cd69873d8960f8d3977abe915ef462aaa84368a7186a3bf in / 
# Wed, 03 May 2023 00:22:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:22:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:23:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:24:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 06:50:35 GMT
ENV LANG=C.UTF-8
# Thu, 04 May 2023 06:50:38 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 06:50:38 GMT
ARG STACK=2.9.3
# Thu, 04 May 2023 06:50:38 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 04 May 2023 06:50:42 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 04 May 2023 06:50:42 GMT
ARG CABAL_INSTALL=3.8.1.0
# Thu, 04 May 2023 06:50:42 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Thu, 04 May 2023 06:50:44 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 04 May 2023 06:54:22 GMT
ARG LLVM_VERSION=12
# Thu, 04 May 2023 06:54:22 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Thu, 04 May 2023 06:54:29 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Thu, 04 May 2023 06:54:30 GMT
ARG GHC=9.0.2
# Thu, 04 May 2023 06:54:30 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 04 May 2023 06:55:17 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 04 May 2023 06:55:27 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 06:55:27 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b7c5fe8e0ac53c77142bf16686fc01d0d2b1fb2da7be5414cdf2f224ec485592`  
		Last Modified: Wed, 03 May 2023 00:26:10 GMT  
		Size: 49.2 MB (49238630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced623c8f9593ccbdc26a5e9ad9d9ad18aa6a8a3b82d7db591552673ac8e3281`  
		Last Modified: Wed, 03 May 2023 17:37:59 GMT  
		Size: 17.5 MB (17450341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fc649f7c89c148c32767dadfc283ae1472705773920b21ddd2bc77d49b2d64`  
		Last Modified: Wed, 03 May 2023 17:38:14 GMT  
		Size: 52.2 MB (52190435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7089b0cf38b0c4474188c7904744a3a55656697b95a3b5088cb510d0e932ba7`  
		Last Modified: Wed, 03 May 2023 17:38:38 GMT  
		Size: 183.5 MB (183454524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b29e6814a3ae5bdbc407544a41b3a6e63f55f582feff0b958bd39a45cac7ea`  
		Last Modified: Thu, 04 May 2023 06:55:45 GMT  
		Size: 517.0 KB (516952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a74f7761e2befcf0d84ef09bdf0daa0a7d4789a63da4f0384d3dc6a7246f1cc`  
		Last Modified: Thu, 04 May 2023 06:55:47 GMT  
		Size: 15.4 MB (15374096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108ebc522e506a00d8bd87318b5a587329490286725a8267770ee95b0caf2273`  
		Last Modified: Thu, 04 May 2023 06:55:47 GMT  
		Size: 12.4 MB (12373196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96492ca2045b78987e28da8694362b2eb28702d35e35aec0c544b55937dbb8fb`  
		Last Modified: Thu, 04 May 2023 06:58:38 GMT  
		Size: 45.9 MB (45889466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dad2a44bfc4145a44a5a9401d87e2284f42e4022978a628b35df00c912811bf`  
		Last Modified: Thu, 04 May 2023 06:59:15 GMT  
		Size: 263.3 MB (263317555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0-buster`

```console
$ docker pull haskell@sha256:798f61d841d1248e51f2a7ef1987d81ac15ffad66fa26734616ab3c3ba3a32d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.0-buster` - linux; amd64

```console
$ docker pull haskell@sha256:bfcfbf5ff336af8bb39b5aa10ba6835ee573dd6fb0e95883588f5ec5e603b0cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **715.4 MB (715437166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ac168ad58549acac147b10b723a69ea0c57645dde84dc0ceba5285f690e2c8`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 01:20:24 GMT
ADD file:9d769df745075dbc4cd2c01ca784571a0df008f6b650b895a7f92d3281132807 in / 
# Tue, 23 May 2023 01:20:25 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:50:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:50:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:52:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:25:03 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 08:25:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:25:08 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 08:25:08 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 08:25:11 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 08:25:11 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 08:25:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 08:25:14 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 08:31:36 GMT
ARG LLVM_VERSION=12
# Tue, 23 May 2023 08:31:36 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 23 May 2023 08:31:36 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 23 May 2023 08:31:36 GMT
ARG GHC=9.0.2
# Tue, 23 May 2023 08:31:37 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 23 May 2023 08:32:48 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 08:32:55 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:32:55 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c722db24a050621ee87ea07acd5d066d3d6a94737c32012f27d73a1ad5cc645c`  
		Last Modified: Tue, 23 May 2023 01:24:26 GMT  
		Size: 50.4 MB (50448716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f8e4a0ed530ff1c74aea38be7ec6c725334c7c3a551b417d0f6f9e220a36fb`  
		Last Modified: Tue, 23 May 2023 01:57:08 GMT  
		Size: 17.6 MB (17580817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a739c67a76c3ff201aa979efc9c5deb081a75f5b98390ee176315cb0cb582aa9`  
		Last Modified: Tue, 23 May 2023 01:57:23 GMT  
		Size: 51.9 MB (51878369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e0d706266f768c6ed028e990dbb063fc43f6028827fe0f39ee6539a963e677`  
		Last Modified: Tue, 23 May 2023 01:57:52 GMT  
		Size: 191.9 MB (191886143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5899d9687951ca93548ece5e39287dc4f5b87d6733a2329490b95ac49b475905`  
		Last Modified: Tue, 23 May 2023 08:34:40 GMT  
		Size: 514.8 KB (514774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729ae0213f5e911798d1f7c2f3be7eaabda44bbf485853229978e6ea41918170`  
		Last Modified: Tue, 23 May 2023 08:34:42 GMT  
		Size: 13.7 MB (13736490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a49eb74c9b4a45e0eaf2f542af477fb0878c8110e8d36e175cb279b0e281636`  
		Last Modified: Tue, 23 May 2023 08:34:42 GMT  
		Size: 7.8 MB (7838367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2635f8f29501aeebff447b4f28162e20c221e95ff6dfe1f2063443c358304d4`  
		Last Modified: Tue, 23 May 2023 08:40:59 GMT  
		Size: 381.6 MB (381553490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.0-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:cf6d9062b0546e88dc415d31385a7c9976a5221182fb508648eb2e1a3635443e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.8 MB (639805195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b9ed0f7adcc993d721155cd76ca0528e1a56d340a3be76a0e28209d2912fe8`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 03 May 2023 00:22:56 GMT
ADD file:6042e29dcf5e22439cd69873d8960f8d3977abe915ef462aaa84368a7186a3bf in / 
# Wed, 03 May 2023 00:22:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:22:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:23:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:24:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 06:50:35 GMT
ENV LANG=C.UTF-8
# Thu, 04 May 2023 06:50:38 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 06:50:38 GMT
ARG STACK=2.9.3
# Thu, 04 May 2023 06:50:38 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 04 May 2023 06:50:42 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 04 May 2023 06:50:42 GMT
ARG CABAL_INSTALL=3.8.1.0
# Thu, 04 May 2023 06:50:42 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Thu, 04 May 2023 06:50:44 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 04 May 2023 06:54:22 GMT
ARG LLVM_VERSION=12
# Thu, 04 May 2023 06:54:22 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Thu, 04 May 2023 06:54:29 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Thu, 04 May 2023 06:54:30 GMT
ARG GHC=9.0.2
# Thu, 04 May 2023 06:54:30 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 04 May 2023 06:55:17 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 04 May 2023 06:55:27 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 06:55:27 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b7c5fe8e0ac53c77142bf16686fc01d0d2b1fb2da7be5414cdf2f224ec485592`  
		Last Modified: Wed, 03 May 2023 00:26:10 GMT  
		Size: 49.2 MB (49238630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced623c8f9593ccbdc26a5e9ad9d9ad18aa6a8a3b82d7db591552673ac8e3281`  
		Last Modified: Wed, 03 May 2023 17:37:59 GMT  
		Size: 17.5 MB (17450341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fc649f7c89c148c32767dadfc283ae1472705773920b21ddd2bc77d49b2d64`  
		Last Modified: Wed, 03 May 2023 17:38:14 GMT  
		Size: 52.2 MB (52190435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7089b0cf38b0c4474188c7904744a3a55656697b95a3b5088cb510d0e932ba7`  
		Last Modified: Wed, 03 May 2023 17:38:38 GMT  
		Size: 183.5 MB (183454524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b29e6814a3ae5bdbc407544a41b3a6e63f55f582feff0b958bd39a45cac7ea`  
		Last Modified: Thu, 04 May 2023 06:55:45 GMT  
		Size: 517.0 KB (516952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a74f7761e2befcf0d84ef09bdf0daa0a7d4789a63da4f0384d3dc6a7246f1cc`  
		Last Modified: Thu, 04 May 2023 06:55:47 GMT  
		Size: 15.4 MB (15374096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108ebc522e506a00d8bd87318b5a587329490286725a8267770ee95b0caf2273`  
		Last Modified: Thu, 04 May 2023 06:55:47 GMT  
		Size: 12.4 MB (12373196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96492ca2045b78987e28da8694362b2eb28702d35e35aec0c544b55937dbb8fb`  
		Last Modified: Thu, 04 May 2023 06:58:38 GMT  
		Size: 45.9 MB (45889466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dad2a44bfc4145a44a5a9401d87e2284f42e4022978a628b35df00c912811bf`  
		Last Modified: Thu, 04 May 2023 06:59:15 GMT  
		Size: 263.3 MB (263317555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0-slim`

```console
$ docker pull haskell@sha256:04b14657063dfb848cc0f91b2c69731b99143601fccc13044cb46051ec7323aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.0-slim` - linux; amd64

```console
$ docker pull haskell@sha256:7a04bf092132da5ac3e1c966487b3a15101f10cdf1645cf14f120b765fc022b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.9 MB (407875650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1386edf1f83d3bbbd2e1a245bc8855047c2a1cb5f0a4efce03c50017dae9ab6a`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 01:20:37 GMT
ADD file:2058e04b33179527a56999678c1c62dfcf76944675afcd77b5163141fb025f8c in / 
# Tue, 23 May 2023 01:20:37 GMT
CMD ["bash"]
# Tue, 23 May 2023 08:26:56 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 08:27:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:27:21 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 08:27:21 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 08:27:24 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 08:27:24 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 08:27:24 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 08:27:27 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 08:32:59 GMT
ARG LLVM_VERSION=12
# Tue, 23 May 2023 08:32:59 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 23 May 2023 08:33:00 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 23 May 2023 08:33:00 GMT
ARG GHC=9.0.2
# Tue, 23 May 2023 08:33:00 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 23 May 2023 08:34:08 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 08:34:14 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:34:14 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:99bf4787315b60d97d860ac6d006b7835b2241a601e93c2da4af6ca554be8704`  
		Last Modified: Tue, 23 May 2023 01:24:47 GMT  
		Size: 27.1 MB (27138577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922ab778f24e7006dd142f8df643984e8c1e678939e7104343f0975f2af889aa`  
		Last Modified: Tue, 23 May 2023 08:36:22 GMT  
		Size: 94.0 MB (94041102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af63a62ebad853e3687cdc43c53fa1acba67c351116e01715a614573acb3b5e`  
		Last Modified: Tue, 23 May 2023 08:36:11 GMT  
		Size: 13.7 MB (13736479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd32594f8ad3cb46719679dc1bec1d16f0fbd03b2fd29976b3b1c386f6e380f`  
		Last Modified: Tue, 23 May 2023 08:36:11 GMT  
		Size: 7.8 MB (7838380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd309e529e093ede4e7e8d1c366e059ba747555a8030a6d41bb3128bb223e2f`  
		Last Modified: Tue, 23 May 2023 08:42:03 GMT  
		Size: 265.1 MB (265121112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.0-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:4416d2af140a0ddfa2419a39a62ee58f489b1ad21a71933d998725fc4a4c2997
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.9 MB (464884181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:188be4dc522fdf3b03d535009b30274323e4fb86427650b3d13ed4f8afde3cc6`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 00:43:28 GMT
ADD file:55a469039df0bf0e94ef7cd2d6fd355ad0c69e0e23e7921194445dd1fe281e3b in / 
# Tue, 23 May 2023 00:43:28 GMT
CMD ["bash"]
# Tue, 23 May 2023 02:13:23 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 02:13:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 02:13:42 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 02:13:42 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 02:13:50 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 02:13:51 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 02:13:51 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 02:13:53 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 02:17:10 GMT
ARG LLVM_VERSION=12
# Tue, 23 May 2023 02:17:10 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 23 May 2023 02:17:18 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 23 May 2023 02:17:19 GMT
ARG GHC=9.0.2
# Tue, 23 May 2023 02:17:19 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 23 May 2023 02:18:03 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 02:18:12 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 02:18:12 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:3ca7b6c7180eac66b9c4301084a16319f41eb7f7365bdf91bcc272bd24cb4149`  
		Last Modified: Tue, 23 May 2023 00:46:44 GMT  
		Size: 25.9 MB (25921744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b1dfa9c7df4de9ed05420bd02fcbf79647f01f988f262f07cb0e1e6d68323d`  
		Last Modified: Tue, 23 May 2023 02:18:44 GMT  
		Size: 88.1 MB (88056276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87343452a5afdee6a1c296325e9b85c3424d00f396673e20fcab8554166166fe`  
		Last Modified: Tue, 23 May 2023 02:18:37 GMT  
		Size: 15.4 MB (15374105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba905b5698eb25fddd7444908f68d9b3bbe45263861f4c5346d9d95da1269fde`  
		Last Modified: Tue, 23 May 2023 02:18:37 GMT  
		Size: 12.4 MB (12373178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e032727cc6f17556b47565b8e599f058e3436656615d511978ccfeaf182a6a59`  
		Last Modified: Tue, 23 May 2023 02:20:44 GMT  
		Size: 59.8 MB (59835792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04057584b58971d241ac1dff04143d23c62e9731d67f905142627fc0ab03d0a`  
		Last Modified: Tue, 23 May 2023 02:21:19 GMT  
		Size: 263.3 MB (263323086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0-slim-buster`

```console
$ docker pull haskell@sha256:04b14657063dfb848cc0f91b2c69731b99143601fccc13044cb46051ec7323aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.0-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:7a04bf092132da5ac3e1c966487b3a15101f10cdf1645cf14f120b765fc022b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.9 MB (407875650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1386edf1f83d3bbbd2e1a245bc8855047c2a1cb5f0a4efce03c50017dae9ab6a`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 01:20:37 GMT
ADD file:2058e04b33179527a56999678c1c62dfcf76944675afcd77b5163141fb025f8c in / 
# Tue, 23 May 2023 01:20:37 GMT
CMD ["bash"]
# Tue, 23 May 2023 08:26:56 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 08:27:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:27:21 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 08:27:21 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 08:27:24 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 08:27:24 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 08:27:24 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 08:27:27 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 08:32:59 GMT
ARG LLVM_VERSION=12
# Tue, 23 May 2023 08:32:59 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 23 May 2023 08:33:00 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 23 May 2023 08:33:00 GMT
ARG GHC=9.0.2
# Tue, 23 May 2023 08:33:00 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 23 May 2023 08:34:08 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 08:34:14 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:34:14 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:99bf4787315b60d97d860ac6d006b7835b2241a601e93c2da4af6ca554be8704`  
		Last Modified: Tue, 23 May 2023 01:24:47 GMT  
		Size: 27.1 MB (27138577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922ab778f24e7006dd142f8df643984e8c1e678939e7104343f0975f2af889aa`  
		Last Modified: Tue, 23 May 2023 08:36:22 GMT  
		Size: 94.0 MB (94041102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af63a62ebad853e3687cdc43c53fa1acba67c351116e01715a614573acb3b5e`  
		Last Modified: Tue, 23 May 2023 08:36:11 GMT  
		Size: 13.7 MB (13736479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd32594f8ad3cb46719679dc1bec1d16f0fbd03b2fd29976b3b1c386f6e380f`  
		Last Modified: Tue, 23 May 2023 08:36:11 GMT  
		Size: 7.8 MB (7838380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd309e529e093ede4e7e8d1c366e059ba747555a8030a6d41bb3128bb223e2f`  
		Last Modified: Tue, 23 May 2023 08:42:03 GMT  
		Size: 265.1 MB (265121112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.0-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:4416d2af140a0ddfa2419a39a62ee58f489b1ad21a71933d998725fc4a4c2997
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.9 MB (464884181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:188be4dc522fdf3b03d535009b30274323e4fb86427650b3d13ed4f8afde3cc6`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 00:43:28 GMT
ADD file:55a469039df0bf0e94ef7cd2d6fd355ad0c69e0e23e7921194445dd1fe281e3b in / 
# Tue, 23 May 2023 00:43:28 GMT
CMD ["bash"]
# Tue, 23 May 2023 02:13:23 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 02:13:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 02:13:42 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 02:13:42 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 02:13:50 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 02:13:51 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 02:13:51 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 02:13:53 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 02:17:10 GMT
ARG LLVM_VERSION=12
# Tue, 23 May 2023 02:17:10 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 23 May 2023 02:17:18 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 23 May 2023 02:17:19 GMT
ARG GHC=9.0.2
# Tue, 23 May 2023 02:17:19 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 23 May 2023 02:18:03 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 02:18:12 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 02:18:12 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:3ca7b6c7180eac66b9c4301084a16319f41eb7f7365bdf91bcc272bd24cb4149`  
		Last Modified: Tue, 23 May 2023 00:46:44 GMT  
		Size: 25.9 MB (25921744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b1dfa9c7df4de9ed05420bd02fcbf79647f01f988f262f07cb0e1e6d68323d`  
		Last Modified: Tue, 23 May 2023 02:18:44 GMT  
		Size: 88.1 MB (88056276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87343452a5afdee6a1c296325e9b85c3424d00f396673e20fcab8554166166fe`  
		Last Modified: Tue, 23 May 2023 02:18:37 GMT  
		Size: 15.4 MB (15374105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba905b5698eb25fddd7444908f68d9b3bbe45263861f4c5346d9d95da1269fde`  
		Last Modified: Tue, 23 May 2023 02:18:37 GMT  
		Size: 12.4 MB (12373178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e032727cc6f17556b47565b8e599f058e3436656615d511978ccfeaf182a6a59`  
		Last Modified: Tue, 23 May 2023 02:20:44 GMT  
		Size: 59.8 MB (59835792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04057584b58971d241ac1dff04143d23c62e9731d67f905142627fc0ab03d0a`  
		Last Modified: Tue, 23 May 2023 02:21:19 GMT  
		Size: 263.3 MB (263323086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0.2`

```console
$ docker pull haskell@sha256:798f61d841d1248e51f2a7ef1987d81ac15ffad66fa26734616ab3c3ba3a32d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.0.2` - linux; amd64

```console
$ docker pull haskell@sha256:bfcfbf5ff336af8bb39b5aa10ba6835ee573dd6fb0e95883588f5ec5e603b0cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **715.4 MB (715437166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ac168ad58549acac147b10b723a69ea0c57645dde84dc0ceba5285f690e2c8`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 01:20:24 GMT
ADD file:9d769df745075dbc4cd2c01ca784571a0df008f6b650b895a7f92d3281132807 in / 
# Tue, 23 May 2023 01:20:25 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:50:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:50:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:52:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:25:03 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 08:25:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:25:08 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 08:25:08 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 08:25:11 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 08:25:11 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 08:25:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 08:25:14 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 08:31:36 GMT
ARG LLVM_VERSION=12
# Tue, 23 May 2023 08:31:36 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 23 May 2023 08:31:36 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 23 May 2023 08:31:36 GMT
ARG GHC=9.0.2
# Tue, 23 May 2023 08:31:37 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 23 May 2023 08:32:48 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 08:32:55 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:32:55 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c722db24a050621ee87ea07acd5d066d3d6a94737c32012f27d73a1ad5cc645c`  
		Last Modified: Tue, 23 May 2023 01:24:26 GMT  
		Size: 50.4 MB (50448716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f8e4a0ed530ff1c74aea38be7ec6c725334c7c3a551b417d0f6f9e220a36fb`  
		Last Modified: Tue, 23 May 2023 01:57:08 GMT  
		Size: 17.6 MB (17580817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a739c67a76c3ff201aa979efc9c5deb081a75f5b98390ee176315cb0cb582aa9`  
		Last Modified: Tue, 23 May 2023 01:57:23 GMT  
		Size: 51.9 MB (51878369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e0d706266f768c6ed028e990dbb063fc43f6028827fe0f39ee6539a963e677`  
		Last Modified: Tue, 23 May 2023 01:57:52 GMT  
		Size: 191.9 MB (191886143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5899d9687951ca93548ece5e39287dc4f5b87d6733a2329490b95ac49b475905`  
		Last Modified: Tue, 23 May 2023 08:34:40 GMT  
		Size: 514.8 KB (514774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729ae0213f5e911798d1f7c2f3be7eaabda44bbf485853229978e6ea41918170`  
		Last Modified: Tue, 23 May 2023 08:34:42 GMT  
		Size: 13.7 MB (13736490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a49eb74c9b4a45e0eaf2f542af477fb0878c8110e8d36e175cb279b0e281636`  
		Last Modified: Tue, 23 May 2023 08:34:42 GMT  
		Size: 7.8 MB (7838367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2635f8f29501aeebff447b4f28162e20c221e95ff6dfe1f2063443c358304d4`  
		Last Modified: Tue, 23 May 2023 08:40:59 GMT  
		Size: 381.6 MB (381553490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.0.2` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:cf6d9062b0546e88dc415d31385a7c9976a5221182fb508648eb2e1a3635443e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.8 MB (639805195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b9ed0f7adcc993d721155cd76ca0528e1a56d340a3be76a0e28209d2912fe8`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 03 May 2023 00:22:56 GMT
ADD file:6042e29dcf5e22439cd69873d8960f8d3977abe915ef462aaa84368a7186a3bf in / 
# Wed, 03 May 2023 00:22:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:22:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:23:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:24:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 06:50:35 GMT
ENV LANG=C.UTF-8
# Thu, 04 May 2023 06:50:38 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 06:50:38 GMT
ARG STACK=2.9.3
# Thu, 04 May 2023 06:50:38 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 04 May 2023 06:50:42 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 04 May 2023 06:50:42 GMT
ARG CABAL_INSTALL=3.8.1.0
# Thu, 04 May 2023 06:50:42 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Thu, 04 May 2023 06:50:44 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 04 May 2023 06:54:22 GMT
ARG LLVM_VERSION=12
# Thu, 04 May 2023 06:54:22 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Thu, 04 May 2023 06:54:29 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Thu, 04 May 2023 06:54:30 GMT
ARG GHC=9.0.2
# Thu, 04 May 2023 06:54:30 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 04 May 2023 06:55:17 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 04 May 2023 06:55:27 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 06:55:27 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b7c5fe8e0ac53c77142bf16686fc01d0d2b1fb2da7be5414cdf2f224ec485592`  
		Last Modified: Wed, 03 May 2023 00:26:10 GMT  
		Size: 49.2 MB (49238630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced623c8f9593ccbdc26a5e9ad9d9ad18aa6a8a3b82d7db591552673ac8e3281`  
		Last Modified: Wed, 03 May 2023 17:37:59 GMT  
		Size: 17.5 MB (17450341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fc649f7c89c148c32767dadfc283ae1472705773920b21ddd2bc77d49b2d64`  
		Last Modified: Wed, 03 May 2023 17:38:14 GMT  
		Size: 52.2 MB (52190435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7089b0cf38b0c4474188c7904744a3a55656697b95a3b5088cb510d0e932ba7`  
		Last Modified: Wed, 03 May 2023 17:38:38 GMT  
		Size: 183.5 MB (183454524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b29e6814a3ae5bdbc407544a41b3a6e63f55f582feff0b958bd39a45cac7ea`  
		Last Modified: Thu, 04 May 2023 06:55:45 GMT  
		Size: 517.0 KB (516952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a74f7761e2befcf0d84ef09bdf0daa0a7d4789a63da4f0384d3dc6a7246f1cc`  
		Last Modified: Thu, 04 May 2023 06:55:47 GMT  
		Size: 15.4 MB (15374096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108ebc522e506a00d8bd87318b5a587329490286725a8267770ee95b0caf2273`  
		Last Modified: Thu, 04 May 2023 06:55:47 GMT  
		Size: 12.4 MB (12373196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96492ca2045b78987e28da8694362b2eb28702d35e35aec0c544b55937dbb8fb`  
		Last Modified: Thu, 04 May 2023 06:58:38 GMT  
		Size: 45.9 MB (45889466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dad2a44bfc4145a44a5a9401d87e2284f42e4022978a628b35df00c912811bf`  
		Last Modified: Thu, 04 May 2023 06:59:15 GMT  
		Size: 263.3 MB (263317555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0.2-buster`

```console
$ docker pull haskell@sha256:798f61d841d1248e51f2a7ef1987d81ac15ffad66fa26734616ab3c3ba3a32d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.0.2-buster` - linux; amd64

```console
$ docker pull haskell@sha256:bfcfbf5ff336af8bb39b5aa10ba6835ee573dd6fb0e95883588f5ec5e603b0cb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **715.4 MB (715437166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ac168ad58549acac147b10b723a69ea0c57645dde84dc0ceba5285f690e2c8`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 01:20:24 GMT
ADD file:9d769df745075dbc4cd2c01ca784571a0df008f6b650b895a7f92d3281132807 in / 
# Tue, 23 May 2023 01:20:25 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:50:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:50:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:52:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:25:03 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 08:25:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:25:08 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 08:25:08 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 08:25:11 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 08:25:11 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 08:25:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 08:25:14 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 08:31:36 GMT
ARG LLVM_VERSION=12
# Tue, 23 May 2023 08:31:36 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 23 May 2023 08:31:36 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 23 May 2023 08:31:36 GMT
ARG GHC=9.0.2
# Tue, 23 May 2023 08:31:37 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 23 May 2023 08:32:48 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 08:32:55 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:32:55 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c722db24a050621ee87ea07acd5d066d3d6a94737c32012f27d73a1ad5cc645c`  
		Last Modified: Tue, 23 May 2023 01:24:26 GMT  
		Size: 50.4 MB (50448716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f8e4a0ed530ff1c74aea38be7ec6c725334c7c3a551b417d0f6f9e220a36fb`  
		Last Modified: Tue, 23 May 2023 01:57:08 GMT  
		Size: 17.6 MB (17580817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a739c67a76c3ff201aa979efc9c5deb081a75f5b98390ee176315cb0cb582aa9`  
		Last Modified: Tue, 23 May 2023 01:57:23 GMT  
		Size: 51.9 MB (51878369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e0d706266f768c6ed028e990dbb063fc43f6028827fe0f39ee6539a963e677`  
		Last Modified: Tue, 23 May 2023 01:57:52 GMT  
		Size: 191.9 MB (191886143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5899d9687951ca93548ece5e39287dc4f5b87d6733a2329490b95ac49b475905`  
		Last Modified: Tue, 23 May 2023 08:34:40 GMT  
		Size: 514.8 KB (514774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729ae0213f5e911798d1f7c2f3be7eaabda44bbf485853229978e6ea41918170`  
		Last Modified: Tue, 23 May 2023 08:34:42 GMT  
		Size: 13.7 MB (13736490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a49eb74c9b4a45e0eaf2f542af477fb0878c8110e8d36e175cb279b0e281636`  
		Last Modified: Tue, 23 May 2023 08:34:42 GMT  
		Size: 7.8 MB (7838367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2635f8f29501aeebff447b4f28162e20c221e95ff6dfe1f2063443c358304d4`  
		Last Modified: Tue, 23 May 2023 08:40:59 GMT  
		Size: 381.6 MB (381553490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.0.2-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:cf6d9062b0546e88dc415d31385a7c9976a5221182fb508648eb2e1a3635443e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.8 MB (639805195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b9ed0f7adcc993d721155cd76ca0528e1a56d340a3be76a0e28209d2912fe8`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 03 May 2023 00:22:56 GMT
ADD file:6042e29dcf5e22439cd69873d8960f8d3977abe915ef462aaa84368a7186a3bf in / 
# Wed, 03 May 2023 00:22:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:22:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:23:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:24:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 06:50:35 GMT
ENV LANG=C.UTF-8
# Thu, 04 May 2023 06:50:38 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 06:50:38 GMT
ARG STACK=2.9.3
# Thu, 04 May 2023 06:50:38 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 04 May 2023 06:50:42 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 04 May 2023 06:50:42 GMT
ARG CABAL_INSTALL=3.8.1.0
# Thu, 04 May 2023 06:50:42 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Thu, 04 May 2023 06:50:44 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 04 May 2023 06:54:22 GMT
ARG LLVM_VERSION=12
# Thu, 04 May 2023 06:54:22 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Thu, 04 May 2023 06:54:29 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Thu, 04 May 2023 06:54:30 GMT
ARG GHC=9.0.2
# Thu, 04 May 2023 06:54:30 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 04 May 2023 06:55:17 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 04 May 2023 06:55:27 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 06:55:27 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b7c5fe8e0ac53c77142bf16686fc01d0d2b1fb2da7be5414cdf2f224ec485592`  
		Last Modified: Wed, 03 May 2023 00:26:10 GMT  
		Size: 49.2 MB (49238630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced623c8f9593ccbdc26a5e9ad9d9ad18aa6a8a3b82d7db591552673ac8e3281`  
		Last Modified: Wed, 03 May 2023 17:37:59 GMT  
		Size: 17.5 MB (17450341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fc649f7c89c148c32767dadfc283ae1472705773920b21ddd2bc77d49b2d64`  
		Last Modified: Wed, 03 May 2023 17:38:14 GMT  
		Size: 52.2 MB (52190435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7089b0cf38b0c4474188c7904744a3a55656697b95a3b5088cb510d0e932ba7`  
		Last Modified: Wed, 03 May 2023 17:38:38 GMT  
		Size: 183.5 MB (183454524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b29e6814a3ae5bdbc407544a41b3a6e63f55f582feff0b958bd39a45cac7ea`  
		Last Modified: Thu, 04 May 2023 06:55:45 GMT  
		Size: 517.0 KB (516952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a74f7761e2befcf0d84ef09bdf0daa0a7d4789a63da4f0384d3dc6a7246f1cc`  
		Last Modified: Thu, 04 May 2023 06:55:47 GMT  
		Size: 15.4 MB (15374096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108ebc522e506a00d8bd87318b5a587329490286725a8267770ee95b0caf2273`  
		Last Modified: Thu, 04 May 2023 06:55:47 GMT  
		Size: 12.4 MB (12373196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96492ca2045b78987e28da8694362b2eb28702d35e35aec0c544b55937dbb8fb`  
		Last Modified: Thu, 04 May 2023 06:58:38 GMT  
		Size: 45.9 MB (45889466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dad2a44bfc4145a44a5a9401d87e2284f42e4022978a628b35df00c912811bf`  
		Last Modified: Thu, 04 May 2023 06:59:15 GMT  
		Size: 263.3 MB (263317555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0.2-slim`

```console
$ docker pull haskell@sha256:04b14657063dfb848cc0f91b2c69731b99143601fccc13044cb46051ec7323aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.0.2-slim` - linux; amd64

```console
$ docker pull haskell@sha256:7a04bf092132da5ac3e1c966487b3a15101f10cdf1645cf14f120b765fc022b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.9 MB (407875650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1386edf1f83d3bbbd2e1a245bc8855047c2a1cb5f0a4efce03c50017dae9ab6a`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 01:20:37 GMT
ADD file:2058e04b33179527a56999678c1c62dfcf76944675afcd77b5163141fb025f8c in / 
# Tue, 23 May 2023 01:20:37 GMT
CMD ["bash"]
# Tue, 23 May 2023 08:26:56 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 08:27:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:27:21 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 08:27:21 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 08:27:24 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 08:27:24 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 08:27:24 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 08:27:27 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 08:32:59 GMT
ARG LLVM_VERSION=12
# Tue, 23 May 2023 08:32:59 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 23 May 2023 08:33:00 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 23 May 2023 08:33:00 GMT
ARG GHC=9.0.2
# Tue, 23 May 2023 08:33:00 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 23 May 2023 08:34:08 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 08:34:14 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:34:14 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:99bf4787315b60d97d860ac6d006b7835b2241a601e93c2da4af6ca554be8704`  
		Last Modified: Tue, 23 May 2023 01:24:47 GMT  
		Size: 27.1 MB (27138577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922ab778f24e7006dd142f8df643984e8c1e678939e7104343f0975f2af889aa`  
		Last Modified: Tue, 23 May 2023 08:36:22 GMT  
		Size: 94.0 MB (94041102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af63a62ebad853e3687cdc43c53fa1acba67c351116e01715a614573acb3b5e`  
		Last Modified: Tue, 23 May 2023 08:36:11 GMT  
		Size: 13.7 MB (13736479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd32594f8ad3cb46719679dc1bec1d16f0fbd03b2fd29976b3b1c386f6e380f`  
		Last Modified: Tue, 23 May 2023 08:36:11 GMT  
		Size: 7.8 MB (7838380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd309e529e093ede4e7e8d1c366e059ba747555a8030a6d41bb3128bb223e2f`  
		Last Modified: Tue, 23 May 2023 08:42:03 GMT  
		Size: 265.1 MB (265121112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.0.2-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:4416d2af140a0ddfa2419a39a62ee58f489b1ad21a71933d998725fc4a4c2997
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.9 MB (464884181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:188be4dc522fdf3b03d535009b30274323e4fb86427650b3d13ed4f8afde3cc6`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 00:43:28 GMT
ADD file:55a469039df0bf0e94ef7cd2d6fd355ad0c69e0e23e7921194445dd1fe281e3b in / 
# Tue, 23 May 2023 00:43:28 GMT
CMD ["bash"]
# Tue, 23 May 2023 02:13:23 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 02:13:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 02:13:42 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 02:13:42 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 02:13:50 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 02:13:51 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 02:13:51 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 02:13:53 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 02:17:10 GMT
ARG LLVM_VERSION=12
# Tue, 23 May 2023 02:17:10 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 23 May 2023 02:17:18 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 23 May 2023 02:17:19 GMT
ARG GHC=9.0.2
# Tue, 23 May 2023 02:17:19 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 23 May 2023 02:18:03 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 02:18:12 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 02:18:12 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:3ca7b6c7180eac66b9c4301084a16319f41eb7f7365bdf91bcc272bd24cb4149`  
		Last Modified: Tue, 23 May 2023 00:46:44 GMT  
		Size: 25.9 MB (25921744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b1dfa9c7df4de9ed05420bd02fcbf79647f01f988f262f07cb0e1e6d68323d`  
		Last Modified: Tue, 23 May 2023 02:18:44 GMT  
		Size: 88.1 MB (88056276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87343452a5afdee6a1c296325e9b85c3424d00f396673e20fcab8554166166fe`  
		Last Modified: Tue, 23 May 2023 02:18:37 GMT  
		Size: 15.4 MB (15374105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba905b5698eb25fddd7444908f68d9b3bbe45263861f4c5346d9d95da1269fde`  
		Last Modified: Tue, 23 May 2023 02:18:37 GMT  
		Size: 12.4 MB (12373178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e032727cc6f17556b47565b8e599f058e3436656615d511978ccfeaf182a6a59`  
		Last Modified: Tue, 23 May 2023 02:20:44 GMT  
		Size: 59.8 MB (59835792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04057584b58971d241ac1dff04143d23c62e9731d67f905142627fc0ab03d0a`  
		Last Modified: Tue, 23 May 2023 02:21:19 GMT  
		Size: 263.3 MB (263323086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0.2-slim-buster`

```console
$ docker pull haskell@sha256:04b14657063dfb848cc0f91b2c69731b99143601fccc13044cb46051ec7323aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.0.2-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:7a04bf092132da5ac3e1c966487b3a15101f10cdf1645cf14f120b765fc022b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.9 MB (407875650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1386edf1f83d3bbbd2e1a245bc8855047c2a1cb5f0a4efce03c50017dae9ab6a`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 01:20:37 GMT
ADD file:2058e04b33179527a56999678c1c62dfcf76944675afcd77b5163141fb025f8c in / 
# Tue, 23 May 2023 01:20:37 GMT
CMD ["bash"]
# Tue, 23 May 2023 08:26:56 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 08:27:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:27:21 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 08:27:21 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 08:27:24 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 08:27:24 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 08:27:24 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 08:27:27 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 08:32:59 GMT
ARG LLVM_VERSION=12
# Tue, 23 May 2023 08:32:59 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 23 May 2023 08:33:00 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 23 May 2023 08:33:00 GMT
ARG GHC=9.0.2
# Tue, 23 May 2023 08:33:00 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 23 May 2023 08:34:08 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 08:34:14 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:34:14 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:99bf4787315b60d97d860ac6d006b7835b2241a601e93c2da4af6ca554be8704`  
		Last Modified: Tue, 23 May 2023 01:24:47 GMT  
		Size: 27.1 MB (27138577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922ab778f24e7006dd142f8df643984e8c1e678939e7104343f0975f2af889aa`  
		Last Modified: Tue, 23 May 2023 08:36:22 GMT  
		Size: 94.0 MB (94041102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af63a62ebad853e3687cdc43c53fa1acba67c351116e01715a614573acb3b5e`  
		Last Modified: Tue, 23 May 2023 08:36:11 GMT  
		Size: 13.7 MB (13736479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd32594f8ad3cb46719679dc1bec1d16f0fbd03b2fd29976b3b1c386f6e380f`  
		Last Modified: Tue, 23 May 2023 08:36:11 GMT  
		Size: 7.8 MB (7838380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd309e529e093ede4e7e8d1c366e059ba747555a8030a6d41bb3128bb223e2f`  
		Last Modified: Tue, 23 May 2023 08:42:03 GMT  
		Size: 265.1 MB (265121112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.0.2-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:4416d2af140a0ddfa2419a39a62ee58f489b1ad21a71933d998725fc4a4c2997
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.9 MB (464884181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:188be4dc522fdf3b03d535009b30274323e4fb86427650b3d13ed4f8afde3cc6`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 00:43:28 GMT
ADD file:55a469039df0bf0e94ef7cd2d6fd355ad0c69e0e23e7921194445dd1fe281e3b in / 
# Tue, 23 May 2023 00:43:28 GMT
CMD ["bash"]
# Tue, 23 May 2023 02:13:23 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 02:13:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 02:13:42 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 02:13:42 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 02:13:50 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 02:13:51 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 02:13:51 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 02:13:53 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 02:17:10 GMT
ARG LLVM_VERSION=12
# Tue, 23 May 2023 02:17:10 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 23 May 2023 02:17:18 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 23 May 2023 02:17:19 GMT
ARG GHC=9.0.2
# Tue, 23 May 2023 02:17:19 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 23 May 2023 02:18:03 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 02:18:12 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 02:18:12 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:3ca7b6c7180eac66b9c4301084a16319f41eb7f7365bdf91bcc272bd24cb4149`  
		Last Modified: Tue, 23 May 2023 00:46:44 GMT  
		Size: 25.9 MB (25921744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b1dfa9c7df4de9ed05420bd02fcbf79647f01f988f262f07cb0e1e6d68323d`  
		Last Modified: Tue, 23 May 2023 02:18:44 GMT  
		Size: 88.1 MB (88056276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87343452a5afdee6a1c296325e9b85c3424d00f396673e20fcab8554166166fe`  
		Last Modified: Tue, 23 May 2023 02:18:37 GMT  
		Size: 15.4 MB (15374105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba905b5698eb25fddd7444908f68d9b3bbe45263861f4c5346d9d95da1269fde`  
		Last Modified: Tue, 23 May 2023 02:18:37 GMT  
		Size: 12.4 MB (12373178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e032727cc6f17556b47565b8e599f058e3436656615d511978ccfeaf182a6a59`  
		Last Modified: Tue, 23 May 2023 02:20:44 GMT  
		Size: 59.8 MB (59835792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04057584b58971d241ac1dff04143d23c62e9731d67f905142627fc0ab03d0a`  
		Last Modified: Tue, 23 May 2023 02:21:19 GMT  
		Size: 263.3 MB (263323086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.2`

```console
$ docker pull haskell@sha256:e29228c0b066c4377453fa38ac5454d1761ff9a361e5707a9278207c52ebf4fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.2` - linux; amd64

```console
$ docker pull haskell@sha256:4855cfc11d78e66368b440103ca9bb04c4e006ffe0b0485f50ca0f2af7dafd37
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **733.4 MB (733384948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c619171d9184517599d9832b985e5670c04a206a876ff774d58bc0e2367cba4`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 01:20:24 GMT
ADD file:9d769df745075dbc4cd2c01ca784571a0df008f6b650b895a7f92d3281132807 in / 
# Tue, 23 May 2023 01:20:25 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:50:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:50:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:52:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:25:03 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 08:25:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:25:08 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 08:25:08 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 08:25:11 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 08:25:11 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 08:25:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 08:25:14 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 08:28:49 GMT
ARG GHC=9.2.7
# Tue, 23 May 2023 08:28:50 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 23 May 2023 08:30:02 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='b4829dd2f4bdaa4b21b22b50edec17616848ab22ab64188047a3eb12bb4da85a';             ;;         'x86_64')             GHC_SHA256='3a76ad6b96915eebf960d1b757ee57341302a76c6a8f97af63fd84eddb45362b';          ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 08:30:09 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:30:09 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c722db24a050621ee87ea07acd5d066d3d6a94737c32012f27d73a1ad5cc645c`  
		Last Modified: Tue, 23 May 2023 01:24:26 GMT  
		Size: 50.4 MB (50448716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f8e4a0ed530ff1c74aea38be7ec6c725334c7c3a551b417d0f6f9e220a36fb`  
		Last Modified: Tue, 23 May 2023 01:57:08 GMT  
		Size: 17.6 MB (17580817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a739c67a76c3ff201aa979efc9c5deb081a75f5b98390ee176315cb0cb582aa9`  
		Last Modified: Tue, 23 May 2023 01:57:23 GMT  
		Size: 51.9 MB (51878369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e0d706266f768c6ed028e990dbb063fc43f6028827fe0f39ee6539a963e677`  
		Last Modified: Tue, 23 May 2023 01:57:52 GMT  
		Size: 191.9 MB (191886143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5899d9687951ca93548ece5e39287dc4f5b87d6733a2329490b95ac49b475905`  
		Last Modified: Tue, 23 May 2023 08:34:40 GMT  
		Size: 514.8 KB (514774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729ae0213f5e911798d1f7c2f3be7eaabda44bbf485853229978e6ea41918170`  
		Last Modified: Tue, 23 May 2023 08:34:42 GMT  
		Size: 13.7 MB (13736490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a49eb74c9b4a45e0eaf2f542af477fb0878c8110e8d36e175cb279b0e281636`  
		Last Modified: Tue, 23 May 2023 08:34:42 GMT  
		Size: 7.8 MB (7838367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213b79af14dfabddb1a735a97ffda8222e014a3d4a587f28cffe33a1cf243b27`  
		Last Modified: Tue, 23 May 2023 08:38:29 GMT  
		Size: 399.5 MB (399501272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.2` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:14bfa59d1a25895a054eb9e88af623d07df1cf99c83a6ddde242dbb8ffd8f231
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **795.3 MB (795290298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3150cc76677c31e4c470ee98acdb8e6513bb13ba4f5034a0d798f0dad42469d`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 03 May 2023 00:22:56 GMT
ADD file:6042e29dcf5e22439cd69873d8960f8d3977abe915ef462aaa84368a7186a3bf in / 
# Wed, 03 May 2023 00:22:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:22:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:23:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:24:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 06:50:35 GMT
ENV LANG=C.UTF-8
# Thu, 04 May 2023 06:50:38 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 06:50:38 GMT
ARG STACK=2.9.3
# Thu, 04 May 2023 06:50:38 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 04 May 2023 06:50:42 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 04 May 2023 06:50:42 GMT
ARG CABAL_INSTALL=3.8.1.0
# Thu, 04 May 2023 06:50:42 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Thu, 04 May 2023 06:50:44 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 04 May 2023 06:52:28 GMT
ARG GHC=9.2.7
# Thu, 04 May 2023 06:52:28 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 04 May 2023 06:53:50 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='b4829dd2f4bdaa4b21b22b50edec17616848ab22ab64188047a3eb12bb4da85a';             ;;         'x86_64')             GHC_SHA256='3a76ad6b96915eebf960d1b757ee57341302a76c6a8f97af63fd84eddb45362b';          ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 04 May 2023 06:54:08 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 06:54:08 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b7c5fe8e0ac53c77142bf16686fc01d0d2b1fb2da7be5414cdf2f224ec485592`  
		Last Modified: Wed, 03 May 2023 00:26:10 GMT  
		Size: 49.2 MB (49238630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced623c8f9593ccbdc26a5e9ad9d9ad18aa6a8a3b82d7db591552673ac8e3281`  
		Last Modified: Wed, 03 May 2023 17:37:59 GMT  
		Size: 17.5 MB (17450341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fc649f7c89c148c32767dadfc283ae1472705773920b21ddd2bc77d49b2d64`  
		Last Modified: Wed, 03 May 2023 17:38:14 GMT  
		Size: 52.2 MB (52190435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7089b0cf38b0c4474188c7904744a3a55656697b95a3b5088cb510d0e932ba7`  
		Last Modified: Wed, 03 May 2023 17:38:38 GMT  
		Size: 183.5 MB (183454524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b29e6814a3ae5bdbc407544a41b3a6e63f55f582feff0b958bd39a45cac7ea`  
		Last Modified: Thu, 04 May 2023 06:55:45 GMT  
		Size: 517.0 KB (516952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a74f7761e2befcf0d84ef09bdf0daa0a7d4789a63da4f0384d3dc6a7246f1cc`  
		Last Modified: Thu, 04 May 2023 06:55:47 GMT  
		Size: 15.4 MB (15374096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108ebc522e506a00d8bd87318b5a587329490286725a8267770ee95b0caf2273`  
		Last Modified: Thu, 04 May 2023 06:55:47 GMT  
		Size: 12.4 MB (12373196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c910f3407dba689181b1e23a03ad754ff5f7616639f9f89493b5e3c2d99b4c2`  
		Last Modified: Thu, 04 May 2023 06:58:21 GMT  
		Size: 464.7 MB (464692124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.2-buster`

```console
$ docker pull haskell@sha256:e29228c0b066c4377453fa38ac5454d1761ff9a361e5707a9278207c52ebf4fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.2-buster` - linux; amd64

```console
$ docker pull haskell@sha256:4855cfc11d78e66368b440103ca9bb04c4e006ffe0b0485f50ca0f2af7dafd37
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **733.4 MB (733384948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c619171d9184517599d9832b985e5670c04a206a876ff774d58bc0e2367cba4`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 01:20:24 GMT
ADD file:9d769df745075dbc4cd2c01ca784571a0df008f6b650b895a7f92d3281132807 in / 
# Tue, 23 May 2023 01:20:25 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:50:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:50:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:52:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:25:03 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 08:25:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:25:08 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 08:25:08 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 08:25:11 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 08:25:11 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 08:25:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 08:25:14 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 08:28:49 GMT
ARG GHC=9.2.7
# Tue, 23 May 2023 08:28:50 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 23 May 2023 08:30:02 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='b4829dd2f4bdaa4b21b22b50edec17616848ab22ab64188047a3eb12bb4da85a';             ;;         'x86_64')             GHC_SHA256='3a76ad6b96915eebf960d1b757ee57341302a76c6a8f97af63fd84eddb45362b';          ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 08:30:09 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:30:09 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c722db24a050621ee87ea07acd5d066d3d6a94737c32012f27d73a1ad5cc645c`  
		Last Modified: Tue, 23 May 2023 01:24:26 GMT  
		Size: 50.4 MB (50448716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f8e4a0ed530ff1c74aea38be7ec6c725334c7c3a551b417d0f6f9e220a36fb`  
		Last Modified: Tue, 23 May 2023 01:57:08 GMT  
		Size: 17.6 MB (17580817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a739c67a76c3ff201aa979efc9c5deb081a75f5b98390ee176315cb0cb582aa9`  
		Last Modified: Tue, 23 May 2023 01:57:23 GMT  
		Size: 51.9 MB (51878369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e0d706266f768c6ed028e990dbb063fc43f6028827fe0f39ee6539a963e677`  
		Last Modified: Tue, 23 May 2023 01:57:52 GMT  
		Size: 191.9 MB (191886143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5899d9687951ca93548ece5e39287dc4f5b87d6733a2329490b95ac49b475905`  
		Last Modified: Tue, 23 May 2023 08:34:40 GMT  
		Size: 514.8 KB (514774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729ae0213f5e911798d1f7c2f3be7eaabda44bbf485853229978e6ea41918170`  
		Last Modified: Tue, 23 May 2023 08:34:42 GMT  
		Size: 13.7 MB (13736490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a49eb74c9b4a45e0eaf2f542af477fb0878c8110e8d36e175cb279b0e281636`  
		Last Modified: Tue, 23 May 2023 08:34:42 GMT  
		Size: 7.8 MB (7838367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213b79af14dfabddb1a735a97ffda8222e014a3d4a587f28cffe33a1cf243b27`  
		Last Modified: Tue, 23 May 2023 08:38:29 GMT  
		Size: 399.5 MB (399501272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.2-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:14bfa59d1a25895a054eb9e88af623d07df1cf99c83a6ddde242dbb8ffd8f231
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **795.3 MB (795290298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3150cc76677c31e4c470ee98acdb8e6513bb13ba4f5034a0d798f0dad42469d`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 03 May 2023 00:22:56 GMT
ADD file:6042e29dcf5e22439cd69873d8960f8d3977abe915ef462aaa84368a7186a3bf in / 
# Wed, 03 May 2023 00:22:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:22:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:23:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:24:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 06:50:35 GMT
ENV LANG=C.UTF-8
# Thu, 04 May 2023 06:50:38 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 06:50:38 GMT
ARG STACK=2.9.3
# Thu, 04 May 2023 06:50:38 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 04 May 2023 06:50:42 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 04 May 2023 06:50:42 GMT
ARG CABAL_INSTALL=3.8.1.0
# Thu, 04 May 2023 06:50:42 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Thu, 04 May 2023 06:50:44 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 04 May 2023 06:52:28 GMT
ARG GHC=9.2.7
# Thu, 04 May 2023 06:52:28 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 04 May 2023 06:53:50 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='b4829dd2f4bdaa4b21b22b50edec17616848ab22ab64188047a3eb12bb4da85a';             ;;         'x86_64')             GHC_SHA256='3a76ad6b96915eebf960d1b757ee57341302a76c6a8f97af63fd84eddb45362b';          ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 04 May 2023 06:54:08 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 06:54:08 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b7c5fe8e0ac53c77142bf16686fc01d0d2b1fb2da7be5414cdf2f224ec485592`  
		Last Modified: Wed, 03 May 2023 00:26:10 GMT  
		Size: 49.2 MB (49238630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced623c8f9593ccbdc26a5e9ad9d9ad18aa6a8a3b82d7db591552673ac8e3281`  
		Last Modified: Wed, 03 May 2023 17:37:59 GMT  
		Size: 17.5 MB (17450341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fc649f7c89c148c32767dadfc283ae1472705773920b21ddd2bc77d49b2d64`  
		Last Modified: Wed, 03 May 2023 17:38:14 GMT  
		Size: 52.2 MB (52190435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7089b0cf38b0c4474188c7904744a3a55656697b95a3b5088cb510d0e932ba7`  
		Last Modified: Wed, 03 May 2023 17:38:38 GMT  
		Size: 183.5 MB (183454524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b29e6814a3ae5bdbc407544a41b3a6e63f55f582feff0b958bd39a45cac7ea`  
		Last Modified: Thu, 04 May 2023 06:55:45 GMT  
		Size: 517.0 KB (516952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a74f7761e2befcf0d84ef09bdf0daa0a7d4789a63da4f0384d3dc6a7246f1cc`  
		Last Modified: Thu, 04 May 2023 06:55:47 GMT  
		Size: 15.4 MB (15374096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108ebc522e506a00d8bd87318b5a587329490286725a8267770ee95b0caf2273`  
		Last Modified: Thu, 04 May 2023 06:55:47 GMT  
		Size: 12.4 MB (12373196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c910f3407dba689181b1e23a03ad754ff5f7616639f9f89493b5e3c2d99b4c2`  
		Last Modified: Thu, 04 May 2023 06:58:21 GMT  
		Size: 464.7 MB (464692124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.2-slim`

```console
$ docker pull haskell@sha256:357cbbbe0442aa2e996588255830f605735b1cb7f554de50bf8cd92b2380babb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.2-slim` - linux; amd64

```console
$ docker pull haskell@sha256:fff4883c450e105250bbbd4a28e39117d0088f8d49349552879919a9fb3a3717
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.2 MB (420238017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5bbbdb9ea3cda41d7c9cb270cf72762a25036dcaae32c1d16e46c31d88b7612`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 01:20:37 GMT
ADD file:2058e04b33179527a56999678c1c62dfcf76944675afcd77b5163141fb025f8c in / 
# Tue, 23 May 2023 01:20:37 GMT
CMD ["bash"]
# Tue, 23 May 2023 08:26:56 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 08:27:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:27:21 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 08:27:21 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 08:27:24 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 08:27:24 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 08:27:24 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 08:27:27 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 08:30:13 GMT
ARG GHC=9.2.7
# Tue, 23 May 2023 08:30:13 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 23 May 2023 08:31:23 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='b4829dd2f4bdaa4b21b22b50edec17616848ab22ab64188047a3eb12bb4da85a';             ;;         'x86_64')             GHC_SHA256='3a76ad6b96915eebf960d1b757ee57341302a76c6a8f97af63fd84eddb45362b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 08:31:29 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:31:29 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:99bf4787315b60d97d860ac6d006b7835b2241a601e93c2da4af6ca554be8704`  
		Last Modified: Tue, 23 May 2023 01:24:47 GMT  
		Size: 27.1 MB (27138577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922ab778f24e7006dd142f8df643984e8c1e678939e7104343f0975f2af889aa`  
		Last Modified: Tue, 23 May 2023 08:36:22 GMT  
		Size: 94.0 MB (94041102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af63a62ebad853e3687cdc43c53fa1acba67c351116e01715a614573acb3b5e`  
		Last Modified: Tue, 23 May 2023 08:36:11 GMT  
		Size: 13.7 MB (13736479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd32594f8ad3cb46719679dc1bec1d16f0fbd03b2fd29976b3b1c386f6e380f`  
		Last Modified: Tue, 23 May 2023 08:36:11 GMT  
		Size: 7.8 MB (7838380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559f2819ea58d8ac7d249e3944469f9f1a7ba9b28511caaa5c0001a2fb8610fc`  
		Last Modified: Tue, 23 May 2023 08:39:35 GMT  
		Size: 277.5 MB (277483479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.2-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:391f775007ebc90e25a9d923bdbc67100a0f208d950e9e6fbdcfe82facf50d05
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.4 MB (461398330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2931f3a7621f8a5f32be7804bb610864a17b412ee200912e27e5f32fd343eef`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 00:43:28 GMT
ADD file:55a469039df0bf0e94ef7cd2d6fd355ad0c69e0e23e7921194445dd1fe281e3b in / 
# Tue, 23 May 2023 00:43:28 GMT
CMD ["bash"]
# Tue, 23 May 2023 02:13:23 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 02:13:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 02:13:42 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 02:13:42 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 02:13:50 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 02:13:51 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 02:13:51 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 02:13:53 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 02:15:31 GMT
ARG GHC=9.2.7
# Tue, 23 May 2023 02:15:31 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 23 May 2023 02:16:53 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='b4829dd2f4bdaa4b21b22b50edec17616848ab22ab64188047a3eb12bb4da85a';             ;;         'x86_64')             GHC_SHA256='3a76ad6b96915eebf960d1b757ee57341302a76c6a8f97af63fd84eddb45362b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 02:17:07 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 02:17:07 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:3ca7b6c7180eac66b9c4301084a16319f41eb7f7365bdf91bcc272bd24cb4149`  
		Last Modified: Tue, 23 May 2023 00:46:44 GMT  
		Size: 25.9 MB (25921744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b1dfa9c7df4de9ed05420bd02fcbf79647f01f988f262f07cb0e1e6d68323d`  
		Last Modified: Tue, 23 May 2023 02:18:44 GMT  
		Size: 88.1 MB (88056276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87343452a5afdee6a1c296325e9b85c3424d00f396673e20fcab8554166166fe`  
		Last Modified: Tue, 23 May 2023 02:18:37 GMT  
		Size: 15.4 MB (15374105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba905b5698eb25fddd7444908f68d9b3bbe45263861f4c5346d9d95da1269fde`  
		Last Modified: Tue, 23 May 2023 02:18:37 GMT  
		Size: 12.4 MB (12373178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42872c7d65e50175c197e09261cc3a34dc2756062d6c204fc693afd3a90cdd17`  
		Last Modified: Tue, 23 May 2023 02:20:24 GMT  
		Size: 319.7 MB (319673027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.2-slim-buster`

```console
$ docker pull haskell@sha256:357cbbbe0442aa2e996588255830f605735b1cb7f554de50bf8cd92b2380babb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.2-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:fff4883c450e105250bbbd4a28e39117d0088f8d49349552879919a9fb3a3717
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.2 MB (420238017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5bbbdb9ea3cda41d7c9cb270cf72762a25036dcaae32c1d16e46c31d88b7612`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 01:20:37 GMT
ADD file:2058e04b33179527a56999678c1c62dfcf76944675afcd77b5163141fb025f8c in / 
# Tue, 23 May 2023 01:20:37 GMT
CMD ["bash"]
# Tue, 23 May 2023 08:26:56 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 08:27:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:27:21 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 08:27:21 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 08:27:24 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 08:27:24 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 08:27:24 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 08:27:27 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 08:30:13 GMT
ARG GHC=9.2.7
# Tue, 23 May 2023 08:30:13 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 23 May 2023 08:31:23 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='b4829dd2f4bdaa4b21b22b50edec17616848ab22ab64188047a3eb12bb4da85a';             ;;         'x86_64')             GHC_SHA256='3a76ad6b96915eebf960d1b757ee57341302a76c6a8f97af63fd84eddb45362b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 08:31:29 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:31:29 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:99bf4787315b60d97d860ac6d006b7835b2241a601e93c2da4af6ca554be8704`  
		Last Modified: Tue, 23 May 2023 01:24:47 GMT  
		Size: 27.1 MB (27138577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922ab778f24e7006dd142f8df643984e8c1e678939e7104343f0975f2af889aa`  
		Last Modified: Tue, 23 May 2023 08:36:22 GMT  
		Size: 94.0 MB (94041102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af63a62ebad853e3687cdc43c53fa1acba67c351116e01715a614573acb3b5e`  
		Last Modified: Tue, 23 May 2023 08:36:11 GMT  
		Size: 13.7 MB (13736479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd32594f8ad3cb46719679dc1bec1d16f0fbd03b2fd29976b3b1c386f6e380f`  
		Last Modified: Tue, 23 May 2023 08:36:11 GMT  
		Size: 7.8 MB (7838380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559f2819ea58d8ac7d249e3944469f9f1a7ba9b28511caaa5c0001a2fb8610fc`  
		Last Modified: Tue, 23 May 2023 08:39:35 GMT  
		Size: 277.5 MB (277483479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.2-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:391f775007ebc90e25a9d923bdbc67100a0f208d950e9e6fbdcfe82facf50d05
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.4 MB (461398330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2931f3a7621f8a5f32be7804bb610864a17b412ee200912e27e5f32fd343eef`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 00:43:28 GMT
ADD file:55a469039df0bf0e94ef7cd2d6fd355ad0c69e0e23e7921194445dd1fe281e3b in / 
# Tue, 23 May 2023 00:43:28 GMT
CMD ["bash"]
# Tue, 23 May 2023 02:13:23 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 02:13:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 02:13:42 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 02:13:42 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 02:13:50 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 02:13:51 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 02:13:51 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 02:13:53 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 02:15:31 GMT
ARG GHC=9.2.7
# Tue, 23 May 2023 02:15:31 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 23 May 2023 02:16:53 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='b4829dd2f4bdaa4b21b22b50edec17616848ab22ab64188047a3eb12bb4da85a';             ;;         'x86_64')             GHC_SHA256='3a76ad6b96915eebf960d1b757ee57341302a76c6a8f97af63fd84eddb45362b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 02:17:07 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 02:17:07 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:3ca7b6c7180eac66b9c4301084a16319f41eb7f7365bdf91bcc272bd24cb4149`  
		Last Modified: Tue, 23 May 2023 00:46:44 GMT  
		Size: 25.9 MB (25921744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b1dfa9c7df4de9ed05420bd02fcbf79647f01f988f262f07cb0e1e6d68323d`  
		Last Modified: Tue, 23 May 2023 02:18:44 GMT  
		Size: 88.1 MB (88056276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87343452a5afdee6a1c296325e9b85c3424d00f396673e20fcab8554166166fe`  
		Last Modified: Tue, 23 May 2023 02:18:37 GMT  
		Size: 15.4 MB (15374105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba905b5698eb25fddd7444908f68d9b3bbe45263861f4c5346d9d95da1269fde`  
		Last Modified: Tue, 23 May 2023 02:18:37 GMT  
		Size: 12.4 MB (12373178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42872c7d65e50175c197e09261cc3a34dc2756062d6c204fc693afd3a90cdd17`  
		Last Modified: Tue, 23 May 2023 02:20:24 GMT  
		Size: 319.7 MB (319673027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.2.7`

```console
$ docker pull haskell@sha256:e29228c0b066c4377453fa38ac5454d1761ff9a361e5707a9278207c52ebf4fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.2.7` - linux; amd64

```console
$ docker pull haskell@sha256:4855cfc11d78e66368b440103ca9bb04c4e006ffe0b0485f50ca0f2af7dafd37
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **733.4 MB (733384948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c619171d9184517599d9832b985e5670c04a206a876ff774d58bc0e2367cba4`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 01:20:24 GMT
ADD file:9d769df745075dbc4cd2c01ca784571a0df008f6b650b895a7f92d3281132807 in / 
# Tue, 23 May 2023 01:20:25 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:50:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:50:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:52:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:25:03 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 08:25:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:25:08 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 08:25:08 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 08:25:11 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 08:25:11 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 08:25:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 08:25:14 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 08:28:49 GMT
ARG GHC=9.2.7
# Tue, 23 May 2023 08:28:50 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 23 May 2023 08:30:02 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='b4829dd2f4bdaa4b21b22b50edec17616848ab22ab64188047a3eb12bb4da85a';             ;;         'x86_64')             GHC_SHA256='3a76ad6b96915eebf960d1b757ee57341302a76c6a8f97af63fd84eddb45362b';          ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 08:30:09 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:30:09 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c722db24a050621ee87ea07acd5d066d3d6a94737c32012f27d73a1ad5cc645c`  
		Last Modified: Tue, 23 May 2023 01:24:26 GMT  
		Size: 50.4 MB (50448716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f8e4a0ed530ff1c74aea38be7ec6c725334c7c3a551b417d0f6f9e220a36fb`  
		Last Modified: Tue, 23 May 2023 01:57:08 GMT  
		Size: 17.6 MB (17580817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a739c67a76c3ff201aa979efc9c5deb081a75f5b98390ee176315cb0cb582aa9`  
		Last Modified: Tue, 23 May 2023 01:57:23 GMT  
		Size: 51.9 MB (51878369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e0d706266f768c6ed028e990dbb063fc43f6028827fe0f39ee6539a963e677`  
		Last Modified: Tue, 23 May 2023 01:57:52 GMT  
		Size: 191.9 MB (191886143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5899d9687951ca93548ece5e39287dc4f5b87d6733a2329490b95ac49b475905`  
		Last Modified: Tue, 23 May 2023 08:34:40 GMT  
		Size: 514.8 KB (514774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729ae0213f5e911798d1f7c2f3be7eaabda44bbf485853229978e6ea41918170`  
		Last Modified: Tue, 23 May 2023 08:34:42 GMT  
		Size: 13.7 MB (13736490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a49eb74c9b4a45e0eaf2f542af477fb0878c8110e8d36e175cb279b0e281636`  
		Last Modified: Tue, 23 May 2023 08:34:42 GMT  
		Size: 7.8 MB (7838367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213b79af14dfabddb1a735a97ffda8222e014a3d4a587f28cffe33a1cf243b27`  
		Last Modified: Tue, 23 May 2023 08:38:29 GMT  
		Size: 399.5 MB (399501272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.2.7` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:14bfa59d1a25895a054eb9e88af623d07df1cf99c83a6ddde242dbb8ffd8f231
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **795.3 MB (795290298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3150cc76677c31e4c470ee98acdb8e6513bb13ba4f5034a0d798f0dad42469d`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 03 May 2023 00:22:56 GMT
ADD file:6042e29dcf5e22439cd69873d8960f8d3977abe915ef462aaa84368a7186a3bf in / 
# Wed, 03 May 2023 00:22:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:22:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:23:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:24:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 06:50:35 GMT
ENV LANG=C.UTF-8
# Thu, 04 May 2023 06:50:38 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 06:50:38 GMT
ARG STACK=2.9.3
# Thu, 04 May 2023 06:50:38 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 04 May 2023 06:50:42 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 04 May 2023 06:50:42 GMT
ARG CABAL_INSTALL=3.8.1.0
# Thu, 04 May 2023 06:50:42 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Thu, 04 May 2023 06:50:44 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 04 May 2023 06:52:28 GMT
ARG GHC=9.2.7
# Thu, 04 May 2023 06:52:28 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 04 May 2023 06:53:50 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='b4829dd2f4bdaa4b21b22b50edec17616848ab22ab64188047a3eb12bb4da85a';             ;;         'x86_64')             GHC_SHA256='3a76ad6b96915eebf960d1b757ee57341302a76c6a8f97af63fd84eddb45362b';          ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 04 May 2023 06:54:08 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 06:54:08 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b7c5fe8e0ac53c77142bf16686fc01d0d2b1fb2da7be5414cdf2f224ec485592`  
		Last Modified: Wed, 03 May 2023 00:26:10 GMT  
		Size: 49.2 MB (49238630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced623c8f9593ccbdc26a5e9ad9d9ad18aa6a8a3b82d7db591552673ac8e3281`  
		Last Modified: Wed, 03 May 2023 17:37:59 GMT  
		Size: 17.5 MB (17450341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fc649f7c89c148c32767dadfc283ae1472705773920b21ddd2bc77d49b2d64`  
		Last Modified: Wed, 03 May 2023 17:38:14 GMT  
		Size: 52.2 MB (52190435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7089b0cf38b0c4474188c7904744a3a55656697b95a3b5088cb510d0e932ba7`  
		Last Modified: Wed, 03 May 2023 17:38:38 GMT  
		Size: 183.5 MB (183454524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b29e6814a3ae5bdbc407544a41b3a6e63f55f582feff0b958bd39a45cac7ea`  
		Last Modified: Thu, 04 May 2023 06:55:45 GMT  
		Size: 517.0 KB (516952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a74f7761e2befcf0d84ef09bdf0daa0a7d4789a63da4f0384d3dc6a7246f1cc`  
		Last Modified: Thu, 04 May 2023 06:55:47 GMT  
		Size: 15.4 MB (15374096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108ebc522e506a00d8bd87318b5a587329490286725a8267770ee95b0caf2273`  
		Last Modified: Thu, 04 May 2023 06:55:47 GMT  
		Size: 12.4 MB (12373196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c910f3407dba689181b1e23a03ad754ff5f7616639f9f89493b5e3c2d99b4c2`  
		Last Modified: Thu, 04 May 2023 06:58:21 GMT  
		Size: 464.7 MB (464692124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.2.7-buster`

```console
$ docker pull haskell@sha256:e29228c0b066c4377453fa38ac5454d1761ff9a361e5707a9278207c52ebf4fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.2.7-buster` - linux; amd64

```console
$ docker pull haskell@sha256:4855cfc11d78e66368b440103ca9bb04c4e006ffe0b0485f50ca0f2af7dafd37
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **733.4 MB (733384948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c619171d9184517599d9832b985e5670c04a206a876ff774d58bc0e2367cba4`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 01:20:24 GMT
ADD file:9d769df745075dbc4cd2c01ca784571a0df008f6b650b895a7f92d3281132807 in / 
# Tue, 23 May 2023 01:20:25 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:50:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:50:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:52:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:25:03 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 08:25:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:25:08 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 08:25:08 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 08:25:11 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 08:25:11 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 08:25:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 08:25:14 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 08:28:49 GMT
ARG GHC=9.2.7
# Tue, 23 May 2023 08:28:50 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 23 May 2023 08:30:02 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='b4829dd2f4bdaa4b21b22b50edec17616848ab22ab64188047a3eb12bb4da85a';             ;;         'x86_64')             GHC_SHA256='3a76ad6b96915eebf960d1b757ee57341302a76c6a8f97af63fd84eddb45362b';          ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 08:30:09 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:30:09 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c722db24a050621ee87ea07acd5d066d3d6a94737c32012f27d73a1ad5cc645c`  
		Last Modified: Tue, 23 May 2023 01:24:26 GMT  
		Size: 50.4 MB (50448716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f8e4a0ed530ff1c74aea38be7ec6c725334c7c3a551b417d0f6f9e220a36fb`  
		Last Modified: Tue, 23 May 2023 01:57:08 GMT  
		Size: 17.6 MB (17580817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a739c67a76c3ff201aa979efc9c5deb081a75f5b98390ee176315cb0cb582aa9`  
		Last Modified: Tue, 23 May 2023 01:57:23 GMT  
		Size: 51.9 MB (51878369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e0d706266f768c6ed028e990dbb063fc43f6028827fe0f39ee6539a963e677`  
		Last Modified: Tue, 23 May 2023 01:57:52 GMT  
		Size: 191.9 MB (191886143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5899d9687951ca93548ece5e39287dc4f5b87d6733a2329490b95ac49b475905`  
		Last Modified: Tue, 23 May 2023 08:34:40 GMT  
		Size: 514.8 KB (514774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729ae0213f5e911798d1f7c2f3be7eaabda44bbf485853229978e6ea41918170`  
		Last Modified: Tue, 23 May 2023 08:34:42 GMT  
		Size: 13.7 MB (13736490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a49eb74c9b4a45e0eaf2f542af477fb0878c8110e8d36e175cb279b0e281636`  
		Last Modified: Tue, 23 May 2023 08:34:42 GMT  
		Size: 7.8 MB (7838367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213b79af14dfabddb1a735a97ffda8222e014a3d4a587f28cffe33a1cf243b27`  
		Last Modified: Tue, 23 May 2023 08:38:29 GMT  
		Size: 399.5 MB (399501272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.2.7-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:14bfa59d1a25895a054eb9e88af623d07df1cf99c83a6ddde242dbb8ffd8f231
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **795.3 MB (795290298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3150cc76677c31e4c470ee98acdb8e6513bb13ba4f5034a0d798f0dad42469d`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 03 May 2023 00:22:56 GMT
ADD file:6042e29dcf5e22439cd69873d8960f8d3977abe915ef462aaa84368a7186a3bf in / 
# Wed, 03 May 2023 00:22:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:22:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:23:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:24:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 06:50:35 GMT
ENV LANG=C.UTF-8
# Thu, 04 May 2023 06:50:38 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 06:50:38 GMT
ARG STACK=2.9.3
# Thu, 04 May 2023 06:50:38 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 04 May 2023 06:50:42 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 04 May 2023 06:50:42 GMT
ARG CABAL_INSTALL=3.8.1.0
# Thu, 04 May 2023 06:50:42 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Thu, 04 May 2023 06:50:44 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 04 May 2023 06:52:28 GMT
ARG GHC=9.2.7
# Thu, 04 May 2023 06:52:28 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 04 May 2023 06:53:50 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='b4829dd2f4bdaa4b21b22b50edec17616848ab22ab64188047a3eb12bb4da85a';             ;;         'x86_64')             GHC_SHA256='3a76ad6b96915eebf960d1b757ee57341302a76c6a8f97af63fd84eddb45362b';          ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 04 May 2023 06:54:08 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 06:54:08 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b7c5fe8e0ac53c77142bf16686fc01d0d2b1fb2da7be5414cdf2f224ec485592`  
		Last Modified: Wed, 03 May 2023 00:26:10 GMT  
		Size: 49.2 MB (49238630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced623c8f9593ccbdc26a5e9ad9d9ad18aa6a8a3b82d7db591552673ac8e3281`  
		Last Modified: Wed, 03 May 2023 17:37:59 GMT  
		Size: 17.5 MB (17450341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fc649f7c89c148c32767dadfc283ae1472705773920b21ddd2bc77d49b2d64`  
		Last Modified: Wed, 03 May 2023 17:38:14 GMT  
		Size: 52.2 MB (52190435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7089b0cf38b0c4474188c7904744a3a55656697b95a3b5088cb510d0e932ba7`  
		Last Modified: Wed, 03 May 2023 17:38:38 GMT  
		Size: 183.5 MB (183454524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b29e6814a3ae5bdbc407544a41b3a6e63f55f582feff0b958bd39a45cac7ea`  
		Last Modified: Thu, 04 May 2023 06:55:45 GMT  
		Size: 517.0 KB (516952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a74f7761e2befcf0d84ef09bdf0daa0a7d4789a63da4f0384d3dc6a7246f1cc`  
		Last Modified: Thu, 04 May 2023 06:55:47 GMT  
		Size: 15.4 MB (15374096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108ebc522e506a00d8bd87318b5a587329490286725a8267770ee95b0caf2273`  
		Last Modified: Thu, 04 May 2023 06:55:47 GMT  
		Size: 12.4 MB (12373196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c910f3407dba689181b1e23a03ad754ff5f7616639f9f89493b5e3c2d99b4c2`  
		Last Modified: Thu, 04 May 2023 06:58:21 GMT  
		Size: 464.7 MB (464692124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.2.7-slim`

```console
$ docker pull haskell@sha256:357cbbbe0442aa2e996588255830f605735b1cb7f554de50bf8cd92b2380babb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.2.7-slim` - linux; amd64

```console
$ docker pull haskell@sha256:fff4883c450e105250bbbd4a28e39117d0088f8d49349552879919a9fb3a3717
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.2 MB (420238017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5bbbdb9ea3cda41d7c9cb270cf72762a25036dcaae32c1d16e46c31d88b7612`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 01:20:37 GMT
ADD file:2058e04b33179527a56999678c1c62dfcf76944675afcd77b5163141fb025f8c in / 
# Tue, 23 May 2023 01:20:37 GMT
CMD ["bash"]
# Tue, 23 May 2023 08:26:56 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 08:27:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:27:21 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 08:27:21 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 08:27:24 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 08:27:24 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 08:27:24 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 08:27:27 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 08:30:13 GMT
ARG GHC=9.2.7
# Tue, 23 May 2023 08:30:13 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 23 May 2023 08:31:23 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='b4829dd2f4bdaa4b21b22b50edec17616848ab22ab64188047a3eb12bb4da85a';             ;;         'x86_64')             GHC_SHA256='3a76ad6b96915eebf960d1b757ee57341302a76c6a8f97af63fd84eddb45362b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 08:31:29 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:31:29 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:99bf4787315b60d97d860ac6d006b7835b2241a601e93c2da4af6ca554be8704`  
		Last Modified: Tue, 23 May 2023 01:24:47 GMT  
		Size: 27.1 MB (27138577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922ab778f24e7006dd142f8df643984e8c1e678939e7104343f0975f2af889aa`  
		Last Modified: Tue, 23 May 2023 08:36:22 GMT  
		Size: 94.0 MB (94041102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af63a62ebad853e3687cdc43c53fa1acba67c351116e01715a614573acb3b5e`  
		Last Modified: Tue, 23 May 2023 08:36:11 GMT  
		Size: 13.7 MB (13736479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd32594f8ad3cb46719679dc1bec1d16f0fbd03b2fd29976b3b1c386f6e380f`  
		Last Modified: Tue, 23 May 2023 08:36:11 GMT  
		Size: 7.8 MB (7838380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559f2819ea58d8ac7d249e3944469f9f1a7ba9b28511caaa5c0001a2fb8610fc`  
		Last Modified: Tue, 23 May 2023 08:39:35 GMT  
		Size: 277.5 MB (277483479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.2.7-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:391f775007ebc90e25a9d923bdbc67100a0f208d950e9e6fbdcfe82facf50d05
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.4 MB (461398330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2931f3a7621f8a5f32be7804bb610864a17b412ee200912e27e5f32fd343eef`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 00:43:28 GMT
ADD file:55a469039df0bf0e94ef7cd2d6fd355ad0c69e0e23e7921194445dd1fe281e3b in / 
# Tue, 23 May 2023 00:43:28 GMT
CMD ["bash"]
# Tue, 23 May 2023 02:13:23 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 02:13:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 02:13:42 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 02:13:42 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 02:13:50 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 02:13:51 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 02:13:51 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 02:13:53 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 02:15:31 GMT
ARG GHC=9.2.7
# Tue, 23 May 2023 02:15:31 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 23 May 2023 02:16:53 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='b4829dd2f4bdaa4b21b22b50edec17616848ab22ab64188047a3eb12bb4da85a';             ;;         'x86_64')             GHC_SHA256='3a76ad6b96915eebf960d1b757ee57341302a76c6a8f97af63fd84eddb45362b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 02:17:07 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 02:17:07 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:3ca7b6c7180eac66b9c4301084a16319f41eb7f7365bdf91bcc272bd24cb4149`  
		Last Modified: Tue, 23 May 2023 00:46:44 GMT  
		Size: 25.9 MB (25921744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b1dfa9c7df4de9ed05420bd02fcbf79647f01f988f262f07cb0e1e6d68323d`  
		Last Modified: Tue, 23 May 2023 02:18:44 GMT  
		Size: 88.1 MB (88056276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87343452a5afdee6a1c296325e9b85c3424d00f396673e20fcab8554166166fe`  
		Last Modified: Tue, 23 May 2023 02:18:37 GMT  
		Size: 15.4 MB (15374105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba905b5698eb25fddd7444908f68d9b3bbe45263861f4c5346d9d95da1269fde`  
		Last Modified: Tue, 23 May 2023 02:18:37 GMT  
		Size: 12.4 MB (12373178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42872c7d65e50175c197e09261cc3a34dc2756062d6c204fc693afd3a90cdd17`  
		Last Modified: Tue, 23 May 2023 02:20:24 GMT  
		Size: 319.7 MB (319673027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.2.7-slim-buster`

```console
$ docker pull haskell@sha256:357cbbbe0442aa2e996588255830f605735b1cb7f554de50bf8cd92b2380babb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.2.7-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:fff4883c450e105250bbbd4a28e39117d0088f8d49349552879919a9fb3a3717
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.2 MB (420238017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5bbbdb9ea3cda41d7c9cb270cf72762a25036dcaae32c1d16e46c31d88b7612`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 01:20:37 GMT
ADD file:2058e04b33179527a56999678c1c62dfcf76944675afcd77b5163141fb025f8c in / 
# Tue, 23 May 2023 01:20:37 GMT
CMD ["bash"]
# Tue, 23 May 2023 08:26:56 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 08:27:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:27:21 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 08:27:21 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 08:27:24 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 08:27:24 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 08:27:24 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 08:27:27 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 08:30:13 GMT
ARG GHC=9.2.7
# Tue, 23 May 2023 08:30:13 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 23 May 2023 08:31:23 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='b4829dd2f4bdaa4b21b22b50edec17616848ab22ab64188047a3eb12bb4da85a';             ;;         'x86_64')             GHC_SHA256='3a76ad6b96915eebf960d1b757ee57341302a76c6a8f97af63fd84eddb45362b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 08:31:29 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:31:29 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:99bf4787315b60d97d860ac6d006b7835b2241a601e93c2da4af6ca554be8704`  
		Last Modified: Tue, 23 May 2023 01:24:47 GMT  
		Size: 27.1 MB (27138577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922ab778f24e7006dd142f8df643984e8c1e678939e7104343f0975f2af889aa`  
		Last Modified: Tue, 23 May 2023 08:36:22 GMT  
		Size: 94.0 MB (94041102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af63a62ebad853e3687cdc43c53fa1acba67c351116e01715a614573acb3b5e`  
		Last Modified: Tue, 23 May 2023 08:36:11 GMT  
		Size: 13.7 MB (13736479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd32594f8ad3cb46719679dc1bec1d16f0fbd03b2fd29976b3b1c386f6e380f`  
		Last Modified: Tue, 23 May 2023 08:36:11 GMT  
		Size: 7.8 MB (7838380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559f2819ea58d8ac7d249e3944469f9f1a7ba9b28511caaa5c0001a2fb8610fc`  
		Last Modified: Tue, 23 May 2023 08:39:35 GMT  
		Size: 277.5 MB (277483479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.2.7-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:391f775007ebc90e25a9d923bdbc67100a0f208d950e9e6fbdcfe82facf50d05
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.4 MB (461398330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2931f3a7621f8a5f32be7804bb610864a17b412ee200912e27e5f32fd343eef`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 00:43:28 GMT
ADD file:55a469039df0bf0e94ef7cd2d6fd355ad0c69e0e23e7921194445dd1fe281e3b in / 
# Tue, 23 May 2023 00:43:28 GMT
CMD ["bash"]
# Tue, 23 May 2023 02:13:23 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 02:13:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 02:13:42 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 02:13:42 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 02:13:50 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 02:13:51 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 02:13:51 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 02:13:53 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 02:15:31 GMT
ARG GHC=9.2.7
# Tue, 23 May 2023 02:15:31 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 23 May 2023 02:16:53 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='b4829dd2f4bdaa4b21b22b50edec17616848ab22ab64188047a3eb12bb4da85a';             ;;         'x86_64')             GHC_SHA256='3a76ad6b96915eebf960d1b757ee57341302a76c6a8f97af63fd84eddb45362b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 02:17:07 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 02:17:07 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:3ca7b6c7180eac66b9c4301084a16319f41eb7f7365bdf91bcc272bd24cb4149`  
		Last Modified: Tue, 23 May 2023 00:46:44 GMT  
		Size: 25.9 MB (25921744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b1dfa9c7df4de9ed05420bd02fcbf79647f01f988f262f07cb0e1e6d68323d`  
		Last Modified: Tue, 23 May 2023 02:18:44 GMT  
		Size: 88.1 MB (88056276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87343452a5afdee6a1c296325e9b85c3424d00f396673e20fcab8554166166fe`  
		Last Modified: Tue, 23 May 2023 02:18:37 GMT  
		Size: 15.4 MB (15374105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba905b5698eb25fddd7444908f68d9b3bbe45263861f4c5346d9d95da1269fde`  
		Last Modified: Tue, 23 May 2023 02:18:37 GMT  
		Size: 12.4 MB (12373178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42872c7d65e50175c197e09261cc3a34dc2756062d6c204fc693afd3a90cdd17`  
		Last Modified: Tue, 23 May 2023 02:20:24 GMT  
		Size: 319.7 MB (319673027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.4`

```console
$ docker pull haskell@sha256:061a6d9588fc9fef00dc758428ee80db3e3d5c0b0b85666adefced246b7ab093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.4` - linux; amd64

```console
$ docker pull haskell@sha256:e8609d28576e5715376ac4e4d12bc1a1680807c003e9b2f11b06a1c94312d193
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **721.3 MB (721262460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e0874f8537eeb3b079a734c33eafbf8ec0254c88e3e219bed678290e5d66d4`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 01:20:24 GMT
ADD file:9d769df745075dbc4cd2c01ca784571a0df008f6b650b895a7f92d3281132807 in / 
# Tue, 23 May 2023 01:20:25 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:50:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:50:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:52:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:25:03 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 08:25:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:25:08 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 08:25:08 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 08:25:11 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 08:25:11 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 08:25:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 08:25:14 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 08:25:14 GMT
ARG GHC=9.4.5
# Tue, 23 May 2023 08:25:14 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Tue, 23 May 2023 08:26:36 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.5 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='ecf16ec503e739e727174b29e5acbe4cf0c54737dd4d5eda046e09323f9ee248';             ;;         'x86_64')             GHC_SHA256='a44c39c4cc9a147de6dd31762995a9e47467cc91757800d80667b8cd60a9b226';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 08:26:43 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.5/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:26:43 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c722db24a050621ee87ea07acd5d066d3d6a94737c32012f27d73a1ad5cc645c`  
		Last Modified: Tue, 23 May 2023 01:24:26 GMT  
		Size: 50.4 MB (50448716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f8e4a0ed530ff1c74aea38be7ec6c725334c7c3a551b417d0f6f9e220a36fb`  
		Last Modified: Tue, 23 May 2023 01:57:08 GMT  
		Size: 17.6 MB (17580817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a739c67a76c3ff201aa979efc9c5deb081a75f5b98390ee176315cb0cb582aa9`  
		Last Modified: Tue, 23 May 2023 01:57:23 GMT  
		Size: 51.9 MB (51878369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e0d706266f768c6ed028e990dbb063fc43f6028827fe0f39ee6539a963e677`  
		Last Modified: Tue, 23 May 2023 01:57:52 GMT  
		Size: 191.9 MB (191886143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5899d9687951ca93548ece5e39287dc4f5b87d6733a2329490b95ac49b475905`  
		Last Modified: Tue, 23 May 2023 08:34:40 GMT  
		Size: 514.8 KB (514774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729ae0213f5e911798d1f7c2f3be7eaabda44bbf485853229978e6ea41918170`  
		Last Modified: Tue, 23 May 2023 08:34:42 GMT  
		Size: 13.7 MB (13736490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a49eb74c9b4a45e0eaf2f542af477fb0878c8110e8d36e175cb279b0e281636`  
		Last Modified: Tue, 23 May 2023 08:34:42 GMT  
		Size: 7.8 MB (7838367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55634913539c42cfcf42734839420cfb08b31a3ba2d1a174dd88894b1114e064`  
		Last Modified: Tue, 23 May 2023 08:35:46 GMT  
		Size: 387.4 MB (387378784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.4` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:c6ff674da0b5d75136bfad35ca6be581c583586625b0fc36f0a256ce0241ed62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **766.2 MB (766222838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77be8ca114cff75846de2efa9954abf091d4d3ac07a82c7d642595fa3f598b8`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 03 May 2023 00:22:56 GMT
ADD file:6042e29dcf5e22439cd69873d8960f8d3977abe915ef462aaa84368a7186a3bf in / 
# Wed, 03 May 2023 00:22:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:22:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:23:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:24:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 06:50:35 GMT
ENV LANG=C.UTF-8
# Thu, 04 May 2023 06:50:38 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 06:50:38 GMT
ARG STACK=2.9.3
# Thu, 04 May 2023 06:50:38 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 04 May 2023 06:50:42 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 04 May 2023 06:50:42 GMT
ARG CABAL_INSTALL=3.8.1.0
# Thu, 04 May 2023 06:50:42 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Thu, 04 May 2023 06:50:44 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 04 May 2023 06:50:44 GMT
ARG GHC=9.4.5
# Thu, 04 May 2023 06:50:44 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Thu, 04 May 2023 06:52:02 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.5 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='ecf16ec503e739e727174b29e5acbe4cf0c54737dd4d5eda046e09323f9ee248';             ;;         'x86_64')             GHC_SHA256='a44c39c4cc9a147de6dd31762995a9e47467cc91757800d80667b8cd60a9b226';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 04 May 2023 06:52:18 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.5/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 06:52:18 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b7c5fe8e0ac53c77142bf16686fc01d0d2b1fb2da7be5414cdf2f224ec485592`  
		Last Modified: Wed, 03 May 2023 00:26:10 GMT  
		Size: 49.2 MB (49238630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced623c8f9593ccbdc26a5e9ad9d9ad18aa6a8a3b82d7db591552673ac8e3281`  
		Last Modified: Wed, 03 May 2023 17:37:59 GMT  
		Size: 17.5 MB (17450341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fc649f7c89c148c32767dadfc283ae1472705773920b21ddd2bc77d49b2d64`  
		Last Modified: Wed, 03 May 2023 17:38:14 GMT  
		Size: 52.2 MB (52190435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7089b0cf38b0c4474188c7904744a3a55656697b95a3b5088cb510d0e932ba7`  
		Last Modified: Wed, 03 May 2023 17:38:38 GMT  
		Size: 183.5 MB (183454524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b29e6814a3ae5bdbc407544a41b3a6e63f55f582feff0b958bd39a45cac7ea`  
		Last Modified: Thu, 04 May 2023 06:55:45 GMT  
		Size: 517.0 KB (516952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a74f7761e2befcf0d84ef09bdf0daa0a7d4789a63da4f0384d3dc6a7246f1cc`  
		Last Modified: Thu, 04 May 2023 06:55:47 GMT  
		Size: 15.4 MB (15374096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108ebc522e506a00d8bd87318b5a587329490286725a8267770ee95b0caf2273`  
		Last Modified: Thu, 04 May 2023 06:55:47 GMT  
		Size: 12.4 MB (12373196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff3ed3db5bee2805f9b104d9e3c2ce074ec04bdd666c74d543802081ed6c5f6`  
		Last Modified: Thu, 04 May 2023 06:56:48 GMT  
		Size: 435.6 MB (435624664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.4-buster`

```console
$ docker pull haskell@sha256:061a6d9588fc9fef00dc758428ee80db3e3d5c0b0b85666adefced246b7ab093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.4-buster` - linux; amd64

```console
$ docker pull haskell@sha256:e8609d28576e5715376ac4e4d12bc1a1680807c003e9b2f11b06a1c94312d193
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **721.3 MB (721262460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e0874f8537eeb3b079a734c33eafbf8ec0254c88e3e219bed678290e5d66d4`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 01:20:24 GMT
ADD file:9d769df745075dbc4cd2c01ca784571a0df008f6b650b895a7f92d3281132807 in / 
# Tue, 23 May 2023 01:20:25 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:50:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:50:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:52:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:25:03 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 08:25:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:25:08 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 08:25:08 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 08:25:11 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 08:25:11 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 08:25:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 08:25:14 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 08:25:14 GMT
ARG GHC=9.4.5
# Tue, 23 May 2023 08:25:14 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Tue, 23 May 2023 08:26:36 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.5 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='ecf16ec503e739e727174b29e5acbe4cf0c54737dd4d5eda046e09323f9ee248';             ;;         'x86_64')             GHC_SHA256='a44c39c4cc9a147de6dd31762995a9e47467cc91757800d80667b8cd60a9b226';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 08:26:43 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.5/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:26:43 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c722db24a050621ee87ea07acd5d066d3d6a94737c32012f27d73a1ad5cc645c`  
		Last Modified: Tue, 23 May 2023 01:24:26 GMT  
		Size: 50.4 MB (50448716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f8e4a0ed530ff1c74aea38be7ec6c725334c7c3a551b417d0f6f9e220a36fb`  
		Last Modified: Tue, 23 May 2023 01:57:08 GMT  
		Size: 17.6 MB (17580817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a739c67a76c3ff201aa979efc9c5deb081a75f5b98390ee176315cb0cb582aa9`  
		Last Modified: Tue, 23 May 2023 01:57:23 GMT  
		Size: 51.9 MB (51878369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e0d706266f768c6ed028e990dbb063fc43f6028827fe0f39ee6539a963e677`  
		Last Modified: Tue, 23 May 2023 01:57:52 GMT  
		Size: 191.9 MB (191886143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5899d9687951ca93548ece5e39287dc4f5b87d6733a2329490b95ac49b475905`  
		Last Modified: Tue, 23 May 2023 08:34:40 GMT  
		Size: 514.8 KB (514774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729ae0213f5e911798d1f7c2f3be7eaabda44bbf485853229978e6ea41918170`  
		Last Modified: Tue, 23 May 2023 08:34:42 GMT  
		Size: 13.7 MB (13736490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a49eb74c9b4a45e0eaf2f542af477fb0878c8110e8d36e175cb279b0e281636`  
		Last Modified: Tue, 23 May 2023 08:34:42 GMT  
		Size: 7.8 MB (7838367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55634913539c42cfcf42734839420cfb08b31a3ba2d1a174dd88894b1114e064`  
		Last Modified: Tue, 23 May 2023 08:35:46 GMT  
		Size: 387.4 MB (387378784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.4-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:c6ff674da0b5d75136bfad35ca6be581c583586625b0fc36f0a256ce0241ed62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **766.2 MB (766222838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77be8ca114cff75846de2efa9954abf091d4d3ac07a82c7d642595fa3f598b8`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 03 May 2023 00:22:56 GMT
ADD file:6042e29dcf5e22439cd69873d8960f8d3977abe915ef462aaa84368a7186a3bf in / 
# Wed, 03 May 2023 00:22:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:22:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:23:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:24:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 06:50:35 GMT
ENV LANG=C.UTF-8
# Thu, 04 May 2023 06:50:38 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 06:50:38 GMT
ARG STACK=2.9.3
# Thu, 04 May 2023 06:50:38 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 04 May 2023 06:50:42 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 04 May 2023 06:50:42 GMT
ARG CABAL_INSTALL=3.8.1.0
# Thu, 04 May 2023 06:50:42 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Thu, 04 May 2023 06:50:44 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 04 May 2023 06:50:44 GMT
ARG GHC=9.4.5
# Thu, 04 May 2023 06:50:44 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Thu, 04 May 2023 06:52:02 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.5 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='ecf16ec503e739e727174b29e5acbe4cf0c54737dd4d5eda046e09323f9ee248';             ;;         'x86_64')             GHC_SHA256='a44c39c4cc9a147de6dd31762995a9e47467cc91757800d80667b8cd60a9b226';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 04 May 2023 06:52:18 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.5/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 06:52:18 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b7c5fe8e0ac53c77142bf16686fc01d0d2b1fb2da7be5414cdf2f224ec485592`  
		Last Modified: Wed, 03 May 2023 00:26:10 GMT  
		Size: 49.2 MB (49238630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced623c8f9593ccbdc26a5e9ad9d9ad18aa6a8a3b82d7db591552673ac8e3281`  
		Last Modified: Wed, 03 May 2023 17:37:59 GMT  
		Size: 17.5 MB (17450341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fc649f7c89c148c32767dadfc283ae1472705773920b21ddd2bc77d49b2d64`  
		Last Modified: Wed, 03 May 2023 17:38:14 GMT  
		Size: 52.2 MB (52190435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7089b0cf38b0c4474188c7904744a3a55656697b95a3b5088cb510d0e932ba7`  
		Last Modified: Wed, 03 May 2023 17:38:38 GMT  
		Size: 183.5 MB (183454524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b29e6814a3ae5bdbc407544a41b3a6e63f55f582feff0b958bd39a45cac7ea`  
		Last Modified: Thu, 04 May 2023 06:55:45 GMT  
		Size: 517.0 KB (516952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a74f7761e2befcf0d84ef09bdf0daa0a7d4789a63da4f0384d3dc6a7246f1cc`  
		Last Modified: Thu, 04 May 2023 06:55:47 GMT  
		Size: 15.4 MB (15374096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108ebc522e506a00d8bd87318b5a587329490286725a8267770ee95b0caf2273`  
		Last Modified: Thu, 04 May 2023 06:55:47 GMT  
		Size: 12.4 MB (12373196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff3ed3db5bee2805f9b104d9e3c2ce074ec04bdd666c74d543802081ed6c5f6`  
		Last Modified: Thu, 04 May 2023 06:56:48 GMT  
		Size: 435.6 MB (435624664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.4-slim`

```console
$ docker pull haskell@sha256:77551349dce35ba3f6f95ad53d736e261ab59b467a3af4164b5bfa51ccebfcce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.4-slim` - linux; amd64

```console
$ docker pull haskell@sha256:89fb63973f87062b26c1cab096f57c5b22b59473ba47f66389ad7ca078e706f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.0 MB (412025721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd594b4728b6f2ba7bb38f2fb399469ef9007208631c554c3e8f71b6f4eda081`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 01:20:37 GMT
ADD file:2058e04b33179527a56999678c1c62dfcf76944675afcd77b5163141fb025f8c in / 
# Tue, 23 May 2023 01:20:37 GMT
CMD ["bash"]
# Tue, 23 May 2023 08:26:56 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 08:27:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:27:21 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 08:27:21 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 08:27:24 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 08:27:24 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 08:27:24 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 08:27:27 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 08:27:27 GMT
ARG GHC=9.4.5
# Tue, 23 May 2023 08:27:27 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Tue, 23 May 2023 08:28:42 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.5 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='ecf16ec503e739e727174b29e5acbe4cf0c54737dd4d5eda046e09323f9ee248';             ;;         'x86_64')             GHC_SHA256='a44c39c4cc9a147de6dd31762995a9e47467cc91757800d80667b8cd60a9b226';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 08:28:47 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.5/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:28:47 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:99bf4787315b60d97d860ac6d006b7835b2241a601e93c2da4af6ca554be8704`  
		Last Modified: Tue, 23 May 2023 01:24:47 GMT  
		Size: 27.1 MB (27138577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922ab778f24e7006dd142f8df643984e8c1e678939e7104343f0975f2af889aa`  
		Last Modified: Tue, 23 May 2023 08:36:22 GMT  
		Size: 94.0 MB (94041102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af63a62ebad853e3687cdc43c53fa1acba67c351116e01715a614573acb3b5e`  
		Last Modified: Tue, 23 May 2023 08:36:11 GMT  
		Size: 13.7 MB (13736479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd32594f8ad3cb46719679dc1bec1d16f0fbd03b2fd29976b3b1c386f6e380f`  
		Last Modified: Tue, 23 May 2023 08:36:11 GMT  
		Size: 7.8 MB (7838380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7690bb755e90f1ef3becc286ac59274aaff9dd6ecf746fad997a95d14a3520b8`  
		Last Modified: Tue, 23 May 2023 08:36:54 GMT  
		Size: 269.3 MB (269271183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.4-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:99eb1374829355eb12431ea07110fa811c4f10a051b5ba43fbfe0eb574f296be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.5 MB (434516775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bbd3cd28aaae40586bf0407842546b69b3f5cc35e0ec70393550258dc83be95`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 00:43:28 GMT
ADD file:55a469039df0bf0e94ef7cd2d6fd355ad0c69e0e23e7921194445dd1fe281e3b in / 
# Tue, 23 May 2023 00:43:28 GMT
CMD ["bash"]
# Tue, 23 May 2023 02:13:23 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 02:13:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 02:13:42 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 02:13:42 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 02:13:50 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 02:13:51 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 02:13:51 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 02:13:53 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 02:13:53 GMT
ARG GHC=9.4.5
# Tue, 23 May 2023 02:13:53 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Tue, 23 May 2023 02:15:10 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.5 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='ecf16ec503e739e727174b29e5acbe4cf0c54737dd4d5eda046e09323f9ee248';             ;;         'x86_64')             GHC_SHA256='a44c39c4cc9a147de6dd31762995a9e47467cc91757800d80667b8cd60a9b226';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 02:15:22 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.5/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 02:15:22 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:3ca7b6c7180eac66b9c4301084a16319f41eb7f7365bdf91bcc272bd24cb4149`  
		Last Modified: Tue, 23 May 2023 00:46:44 GMT  
		Size: 25.9 MB (25921744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b1dfa9c7df4de9ed05420bd02fcbf79647f01f988f262f07cb0e1e6d68323d`  
		Last Modified: Tue, 23 May 2023 02:18:44 GMT  
		Size: 88.1 MB (88056276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87343452a5afdee6a1c296325e9b85c3424d00f396673e20fcab8554166166fe`  
		Last Modified: Tue, 23 May 2023 02:18:37 GMT  
		Size: 15.4 MB (15374105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba905b5698eb25fddd7444908f68d9b3bbe45263861f4c5346d9d95da1269fde`  
		Last Modified: Tue, 23 May 2023 02:18:37 GMT  
		Size: 12.4 MB (12373178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ff7a6c59b9c4ebd1c4fe70ce63a4eb0eaa932fa606622bf1fb0a68e6be1ea5`  
		Last Modified: Tue, 23 May 2023 02:19:15 GMT  
		Size: 292.8 MB (292791472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.4-slim-buster`

```console
$ docker pull haskell@sha256:77551349dce35ba3f6f95ad53d736e261ab59b467a3af4164b5bfa51ccebfcce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.4-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:89fb63973f87062b26c1cab096f57c5b22b59473ba47f66389ad7ca078e706f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.0 MB (412025721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd594b4728b6f2ba7bb38f2fb399469ef9007208631c554c3e8f71b6f4eda081`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 01:20:37 GMT
ADD file:2058e04b33179527a56999678c1c62dfcf76944675afcd77b5163141fb025f8c in / 
# Tue, 23 May 2023 01:20:37 GMT
CMD ["bash"]
# Tue, 23 May 2023 08:26:56 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 08:27:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:27:21 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 08:27:21 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 08:27:24 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 08:27:24 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 08:27:24 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 08:27:27 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 08:27:27 GMT
ARG GHC=9.4.5
# Tue, 23 May 2023 08:27:27 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Tue, 23 May 2023 08:28:42 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.5 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='ecf16ec503e739e727174b29e5acbe4cf0c54737dd4d5eda046e09323f9ee248';             ;;         'x86_64')             GHC_SHA256='a44c39c4cc9a147de6dd31762995a9e47467cc91757800d80667b8cd60a9b226';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 08:28:47 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.5/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:28:47 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:99bf4787315b60d97d860ac6d006b7835b2241a601e93c2da4af6ca554be8704`  
		Last Modified: Tue, 23 May 2023 01:24:47 GMT  
		Size: 27.1 MB (27138577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922ab778f24e7006dd142f8df643984e8c1e678939e7104343f0975f2af889aa`  
		Last Modified: Tue, 23 May 2023 08:36:22 GMT  
		Size: 94.0 MB (94041102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af63a62ebad853e3687cdc43c53fa1acba67c351116e01715a614573acb3b5e`  
		Last Modified: Tue, 23 May 2023 08:36:11 GMT  
		Size: 13.7 MB (13736479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd32594f8ad3cb46719679dc1bec1d16f0fbd03b2fd29976b3b1c386f6e380f`  
		Last Modified: Tue, 23 May 2023 08:36:11 GMT  
		Size: 7.8 MB (7838380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7690bb755e90f1ef3becc286ac59274aaff9dd6ecf746fad997a95d14a3520b8`  
		Last Modified: Tue, 23 May 2023 08:36:54 GMT  
		Size: 269.3 MB (269271183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.4-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:99eb1374829355eb12431ea07110fa811c4f10a051b5ba43fbfe0eb574f296be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.5 MB (434516775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bbd3cd28aaae40586bf0407842546b69b3f5cc35e0ec70393550258dc83be95`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 00:43:28 GMT
ADD file:55a469039df0bf0e94ef7cd2d6fd355ad0c69e0e23e7921194445dd1fe281e3b in / 
# Tue, 23 May 2023 00:43:28 GMT
CMD ["bash"]
# Tue, 23 May 2023 02:13:23 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 02:13:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 02:13:42 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 02:13:42 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 02:13:50 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 02:13:51 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 02:13:51 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 02:13:53 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 02:13:53 GMT
ARG GHC=9.4.5
# Tue, 23 May 2023 02:13:53 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Tue, 23 May 2023 02:15:10 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.5 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='ecf16ec503e739e727174b29e5acbe4cf0c54737dd4d5eda046e09323f9ee248';             ;;         'x86_64')             GHC_SHA256='a44c39c4cc9a147de6dd31762995a9e47467cc91757800d80667b8cd60a9b226';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 02:15:22 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.5/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 02:15:22 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:3ca7b6c7180eac66b9c4301084a16319f41eb7f7365bdf91bcc272bd24cb4149`  
		Last Modified: Tue, 23 May 2023 00:46:44 GMT  
		Size: 25.9 MB (25921744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b1dfa9c7df4de9ed05420bd02fcbf79647f01f988f262f07cb0e1e6d68323d`  
		Last Modified: Tue, 23 May 2023 02:18:44 GMT  
		Size: 88.1 MB (88056276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87343452a5afdee6a1c296325e9b85c3424d00f396673e20fcab8554166166fe`  
		Last Modified: Tue, 23 May 2023 02:18:37 GMT  
		Size: 15.4 MB (15374105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba905b5698eb25fddd7444908f68d9b3bbe45263861f4c5346d9d95da1269fde`  
		Last Modified: Tue, 23 May 2023 02:18:37 GMT  
		Size: 12.4 MB (12373178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ff7a6c59b9c4ebd1c4fe70ce63a4eb0eaa932fa606622bf1fb0a68e6be1ea5`  
		Last Modified: Tue, 23 May 2023 02:19:15 GMT  
		Size: 292.8 MB (292791472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.4.5`

```console
$ docker pull haskell@sha256:061a6d9588fc9fef00dc758428ee80db3e3d5c0b0b85666adefced246b7ab093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.4.5` - linux; amd64

```console
$ docker pull haskell@sha256:e8609d28576e5715376ac4e4d12bc1a1680807c003e9b2f11b06a1c94312d193
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **721.3 MB (721262460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e0874f8537eeb3b079a734c33eafbf8ec0254c88e3e219bed678290e5d66d4`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 01:20:24 GMT
ADD file:9d769df745075dbc4cd2c01ca784571a0df008f6b650b895a7f92d3281132807 in / 
# Tue, 23 May 2023 01:20:25 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:50:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:50:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:52:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:25:03 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 08:25:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:25:08 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 08:25:08 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 08:25:11 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 08:25:11 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 08:25:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 08:25:14 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 08:25:14 GMT
ARG GHC=9.4.5
# Tue, 23 May 2023 08:25:14 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Tue, 23 May 2023 08:26:36 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.5 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='ecf16ec503e739e727174b29e5acbe4cf0c54737dd4d5eda046e09323f9ee248';             ;;         'x86_64')             GHC_SHA256='a44c39c4cc9a147de6dd31762995a9e47467cc91757800d80667b8cd60a9b226';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 08:26:43 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.5/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:26:43 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c722db24a050621ee87ea07acd5d066d3d6a94737c32012f27d73a1ad5cc645c`  
		Last Modified: Tue, 23 May 2023 01:24:26 GMT  
		Size: 50.4 MB (50448716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f8e4a0ed530ff1c74aea38be7ec6c725334c7c3a551b417d0f6f9e220a36fb`  
		Last Modified: Tue, 23 May 2023 01:57:08 GMT  
		Size: 17.6 MB (17580817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a739c67a76c3ff201aa979efc9c5deb081a75f5b98390ee176315cb0cb582aa9`  
		Last Modified: Tue, 23 May 2023 01:57:23 GMT  
		Size: 51.9 MB (51878369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e0d706266f768c6ed028e990dbb063fc43f6028827fe0f39ee6539a963e677`  
		Last Modified: Tue, 23 May 2023 01:57:52 GMT  
		Size: 191.9 MB (191886143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5899d9687951ca93548ece5e39287dc4f5b87d6733a2329490b95ac49b475905`  
		Last Modified: Tue, 23 May 2023 08:34:40 GMT  
		Size: 514.8 KB (514774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729ae0213f5e911798d1f7c2f3be7eaabda44bbf485853229978e6ea41918170`  
		Last Modified: Tue, 23 May 2023 08:34:42 GMT  
		Size: 13.7 MB (13736490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a49eb74c9b4a45e0eaf2f542af477fb0878c8110e8d36e175cb279b0e281636`  
		Last Modified: Tue, 23 May 2023 08:34:42 GMT  
		Size: 7.8 MB (7838367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55634913539c42cfcf42734839420cfb08b31a3ba2d1a174dd88894b1114e064`  
		Last Modified: Tue, 23 May 2023 08:35:46 GMT  
		Size: 387.4 MB (387378784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.4.5` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:c6ff674da0b5d75136bfad35ca6be581c583586625b0fc36f0a256ce0241ed62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **766.2 MB (766222838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77be8ca114cff75846de2efa9954abf091d4d3ac07a82c7d642595fa3f598b8`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 03 May 2023 00:22:56 GMT
ADD file:6042e29dcf5e22439cd69873d8960f8d3977abe915ef462aaa84368a7186a3bf in / 
# Wed, 03 May 2023 00:22:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:22:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:23:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:24:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 06:50:35 GMT
ENV LANG=C.UTF-8
# Thu, 04 May 2023 06:50:38 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 06:50:38 GMT
ARG STACK=2.9.3
# Thu, 04 May 2023 06:50:38 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 04 May 2023 06:50:42 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 04 May 2023 06:50:42 GMT
ARG CABAL_INSTALL=3.8.1.0
# Thu, 04 May 2023 06:50:42 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Thu, 04 May 2023 06:50:44 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 04 May 2023 06:50:44 GMT
ARG GHC=9.4.5
# Thu, 04 May 2023 06:50:44 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Thu, 04 May 2023 06:52:02 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.5 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='ecf16ec503e739e727174b29e5acbe4cf0c54737dd4d5eda046e09323f9ee248';             ;;         'x86_64')             GHC_SHA256='a44c39c4cc9a147de6dd31762995a9e47467cc91757800d80667b8cd60a9b226';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 04 May 2023 06:52:18 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.5/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 06:52:18 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b7c5fe8e0ac53c77142bf16686fc01d0d2b1fb2da7be5414cdf2f224ec485592`  
		Last Modified: Wed, 03 May 2023 00:26:10 GMT  
		Size: 49.2 MB (49238630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced623c8f9593ccbdc26a5e9ad9d9ad18aa6a8a3b82d7db591552673ac8e3281`  
		Last Modified: Wed, 03 May 2023 17:37:59 GMT  
		Size: 17.5 MB (17450341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fc649f7c89c148c32767dadfc283ae1472705773920b21ddd2bc77d49b2d64`  
		Last Modified: Wed, 03 May 2023 17:38:14 GMT  
		Size: 52.2 MB (52190435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7089b0cf38b0c4474188c7904744a3a55656697b95a3b5088cb510d0e932ba7`  
		Last Modified: Wed, 03 May 2023 17:38:38 GMT  
		Size: 183.5 MB (183454524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b29e6814a3ae5bdbc407544a41b3a6e63f55f582feff0b958bd39a45cac7ea`  
		Last Modified: Thu, 04 May 2023 06:55:45 GMT  
		Size: 517.0 KB (516952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a74f7761e2befcf0d84ef09bdf0daa0a7d4789a63da4f0384d3dc6a7246f1cc`  
		Last Modified: Thu, 04 May 2023 06:55:47 GMT  
		Size: 15.4 MB (15374096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108ebc522e506a00d8bd87318b5a587329490286725a8267770ee95b0caf2273`  
		Last Modified: Thu, 04 May 2023 06:55:47 GMT  
		Size: 12.4 MB (12373196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff3ed3db5bee2805f9b104d9e3c2ce074ec04bdd666c74d543802081ed6c5f6`  
		Last Modified: Thu, 04 May 2023 06:56:48 GMT  
		Size: 435.6 MB (435624664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.4.5-buster`

```console
$ docker pull haskell@sha256:061a6d9588fc9fef00dc758428ee80db3e3d5c0b0b85666adefced246b7ab093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.4.5-buster` - linux; amd64

```console
$ docker pull haskell@sha256:e8609d28576e5715376ac4e4d12bc1a1680807c003e9b2f11b06a1c94312d193
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **721.3 MB (721262460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e0874f8537eeb3b079a734c33eafbf8ec0254c88e3e219bed678290e5d66d4`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 01:20:24 GMT
ADD file:9d769df745075dbc4cd2c01ca784571a0df008f6b650b895a7f92d3281132807 in / 
# Tue, 23 May 2023 01:20:25 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:50:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:50:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:52:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:25:03 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 08:25:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:25:08 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 08:25:08 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 08:25:11 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 08:25:11 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 08:25:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 08:25:14 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 08:25:14 GMT
ARG GHC=9.4.5
# Tue, 23 May 2023 08:25:14 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Tue, 23 May 2023 08:26:36 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.5 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='ecf16ec503e739e727174b29e5acbe4cf0c54737dd4d5eda046e09323f9ee248';             ;;         'x86_64')             GHC_SHA256='a44c39c4cc9a147de6dd31762995a9e47467cc91757800d80667b8cd60a9b226';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 08:26:43 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.5/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:26:43 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c722db24a050621ee87ea07acd5d066d3d6a94737c32012f27d73a1ad5cc645c`  
		Last Modified: Tue, 23 May 2023 01:24:26 GMT  
		Size: 50.4 MB (50448716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f8e4a0ed530ff1c74aea38be7ec6c725334c7c3a551b417d0f6f9e220a36fb`  
		Last Modified: Tue, 23 May 2023 01:57:08 GMT  
		Size: 17.6 MB (17580817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a739c67a76c3ff201aa979efc9c5deb081a75f5b98390ee176315cb0cb582aa9`  
		Last Modified: Tue, 23 May 2023 01:57:23 GMT  
		Size: 51.9 MB (51878369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e0d706266f768c6ed028e990dbb063fc43f6028827fe0f39ee6539a963e677`  
		Last Modified: Tue, 23 May 2023 01:57:52 GMT  
		Size: 191.9 MB (191886143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5899d9687951ca93548ece5e39287dc4f5b87d6733a2329490b95ac49b475905`  
		Last Modified: Tue, 23 May 2023 08:34:40 GMT  
		Size: 514.8 KB (514774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729ae0213f5e911798d1f7c2f3be7eaabda44bbf485853229978e6ea41918170`  
		Last Modified: Tue, 23 May 2023 08:34:42 GMT  
		Size: 13.7 MB (13736490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a49eb74c9b4a45e0eaf2f542af477fb0878c8110e8d36e175cb279b0e281636`  
		Last Modified: Tue, 23 May 2023 08:34:42 GMT  
		Size: 7.8 MB (7838367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55634913539c42cfcf42734839420cfb08b31a3ba2d1a174dd88894b1114e064`  
		Last Modified: Tue, 23 May 2023 08:35:46 GMT  
		Size: 387.4 MB (387378784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.4.5-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:c6ff674da0b5d75136bfad35ca6be581c583586625b0fc36f0a256ce0241ed62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **766.2 MB (766222838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77be8ca114cff75846de2efa9954abf091d4d3ac07a82c7d642595fa3f598b8`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 03 May 2023 00:22:56 GMT
ADD file:6042e29dcf5e22439cd69873d8960f8d3977abe915ef462aaa84368a7186a3bf in / 
# Wed, 03 May 2023 00:22:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:22:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:23:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:24:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 06:50:35 GMT
ENV LANG=C.UTF-8
# Thu, 04 May 2023 06:50:38 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 06:50:38 GMT
ARG STACK=2.9.3
# Thu, 04 May 2023 06:50:38 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 04 May 2023 06:50:42 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 04 May 2023 06:50:42 GMT
ARG CABAL_INSTALL=3.8.1.0
# Thu, 04 May 2023 06:50:42 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Thu, 04 May 2023 06:50:44 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 04 May 2023 06:50:44 GMT
ARG GHC=9.4.5
# Thu, 04 May 2023 06:50:44 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Thu, 04 May 2023 06:52:02 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.5 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='ecf16ec503e739e727174b29e5acbe4cf0c54737dd4d5eda046e09323f9ee248';             ;;         'x86_64')             GHC_SHA256='a44c39c4cc9a147de6dd31762995a9e47467cc91757800d80667b8cd60a9b226';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 04 May 2023 06:52:18 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.5/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 06:52:18 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b7c5fe8e0ac53c77142bf16686fc01d0d2b1fb2da7be5414cdf2f224ec485592`  
		Last Modified: Wed, 03 May 2023 00:26:10 GMT  
		Size: 49.2 MB (49238630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced623c8f9593ccbdc26a5e9ad9d9ad18aa6a8a3b82d7db591552673ac8e3281`  
		Last Modified: Wed, 03 May 2023 17:37:59 GMT  
		Size: 17.5 MB (17450341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fc649f7c89c148c32767dadfc283ae1472705773920b21ddd2bc77d49b2d64`  
		Last Modified: Wed, 03 May 2023 17:38:14 GMT  
		Size: 52.2 MB (52190435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7089b0cf38b0c4474188c7904744a3a55656697b95a3b5088cb510d0e932ba7`  
		Last Modified: Wed, 03 May 2023 17:38:38 GMT  
		Size: 183.5 MB (183454524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b29e6814a3ae5bdbc407544a41b3a6e63f55f582feff0b958bd39a45cac7ea`  
		Last Modified: Thu, 04 May 2023 06:55:45 GMT  
		Size: 517.0 KB (516952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a74f7761e2befcf0d84ef09bdf0daa0a7d4789a63da4f0384d3dc6a7246f1cc`  
		Last Modified: Thu, 04 May 2023 06:55:47 GMT  
		Size: 15.4 MB (15374096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108ebc522e506a00d8bd87318b5a587329490286725a8267770ee95b0caf2273`  
		Last Modified: Thu, 04 May 2023 06:55:47 GMT  
		Size: 12.4 MB (12373196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff3ed3db5bee2805f9b104d9e3c2ce074ec04bdd666c74d543802081ed6c5f6`  
		Last Modified: Thu, 04 May 2023 06:56:48 GMT  
		Size: 435.6 MB (435624664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.4.5-slim`

```console
$ docker pull haskell@sha256:77551349dce35ba3f6f95ad53d736e261ab59b467a3af4164b5bfa51ccebfcce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.4.5-slim` - linux; amd64

```console
$ docker pull haskell@sha256:89fb63973f87062b26c1cab096f57c5b22b59473ba47f66389ad7ca078e706f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.0 MB (412025721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd594b4728b6f2ba7bb38f2fb399469ef9007208631c554c3e8f71b6f4eda081`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 01:20:37 GMT
ADD file:2058e04b33179527a56999678c1c62dfcf76944675afcd77b5163141fb025f8c in / 
# Tue, 23 May 2023 01:20:37 GMT
CMD ["bash"]
# Tue, 23 May 2023 08:26:56 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 08:27:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:27:21 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 08:27:21 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 08:27:24 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 08:27:24 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 08:27:24 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 08:27:27 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 08:27:27 GMT
ARG GHC=9.4.5
# Tue, 23 May 2023 08:27:27 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Tue, 23 May 2023 08:28:42 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.5 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='ecf16ec503e739e727174b29e5acbe4cf0c54737dd4d5eda046e09323f9ee248';             ;;         'x86_64')             GHC_SHA256='a44c39c4cc9a147de6dd31762995a9e47467cc91757800d80667b8cd60a9b226';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 08:28:47 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.5/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:28:47 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:99bf4787315b60d97d860ac6d006b7835b2241a601e93c2da4af6ca554be8704`  
		Last Modified: Tue, 23 May 2023 01:24:47 GMT  
		Size: 27.1 MB (27138577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922ab778f24e7006dd142f8df643984e8c1e678939e7104343f0975f2af889aa`  
		Last Modified: Tue, 23 May 2023 08:36:22 GMT  
		Size: 94.0 MB (94041102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af63a62ebad853e3687cdc43c53fa1acba67c351116e01715a614573acb3b5e`  
		Last Modified: Tue, 23 May 2023 08:36:11 GMT  
		Size: 13.7 MB (13736479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd32594f8ad3cb46719679dc1bec1d16f0fbd03b2fd29976b3b1c386f6e380f`  
		Last Modified: Tue, 23 May 2023 08:36:11 GMT  
		Size: 7.8 MB (7838380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7690bb755e90f1ef3becc286ac59274aaff9dd6ecf746fad997a95d14a3520b8`  
		Last Modified: Tue, 23 May 2023 08:36:54 GMT  
		Size: 269.3 MB (269271183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.4.5-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:99eb1374829355eb12431ea07110fa811c4f10a051b5ba43fbfe0eb574f296be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.5 MB (434516775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bbd3cd28aaae40586bf0407842546b69b3f5cc35e0ec70393550258dc83be95`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 00:43:28 GMT
ADD file:55a469039df0bf0e94ef7cd2d6fd355ad0c69e0e23e7921194445dd1fe281e3b in / 
# Tue, 23 May 2023 00:43:28 GMT
CMD ["bash"]
# Tue, 23 May 2023 02:13:23 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 02:13:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 02:13:42 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 02:13:42 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 02:13:50 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 02:13:51 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 02:13:51 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 02:13:53 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 02:13:53 GMT
ARG GHC=9.4.5
# Tue, 23 May 2023 02:13:53 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Tue, 23 May 2023 02:15:10 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.5 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='ecf16ec503e739e727174b29e5acbe4cf0c54737dd4d5eda046e09323f9ee248';             ;;         'x86_64')             GHC_SHA256='a44c39c4cc9a147de6dd31762995a9e47467cc91757800d80667b8cd60a9b226';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 02:15:22 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.5/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 02:15:22 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:3ca7b6c7180eac66b9c4301084a16319f41eb7f7365bdf91bcc272bd24cb4149`  
		Last Modified: Tue, 23 May 2023 00:46:44 GMT  
		Size: 25.9 MB (25921744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b1dfa9c7df4de9ed05420bd02fcbf79647f01f988f262f07cb0e1e6d68323d`  
		Last Modified: Tue, 23 May 2023 02:18:44 GMT  
		Size: 88.1 MB (88056276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87343452a5afdee6a1c296325e9b85c3424d00f396673e20fcab8554166166fe`  
		Last Modified: Tue, 23 May 2023 02:18:37 GMT  
		Size: 15.4 MB (15374105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba905b5698eb25fddd7444908f68d9b3bbe45263861f4c5346d9d95da1269fde`  
		Last Modified: Tue, 23 May 2023 02:18:37 GMT  
		Size: 12.4 MB (12373178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ff7a6c59b9c4ebd1c4fe70ce63a4eb0eaa932fa606622bf1fb0a68e6be1ea5`  
		Last Modified: Tue, 23 May 2023 02:19:15 GMT  
		Size: 292.8 MB (292791472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.4.5-slim-buster`

```console
$ docker pull haskell@sha256:77551349dce35ba3f6f95ad53d736e261ab59b467a3af4164b5bfa51ccebfcce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.4.5-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:89fb63973f87062b26c1cab096f57c5b22b59473ba47f66389ad7ca078e706f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.0 MB (412025721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd594b4728b6f2ba7bb38f2fb399469ef9007208631c554c3e8f71b6f4eda081`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 01:20:37 GMT
ADD file:2058e04b33179527a56999678c1c62dfcf76944675afcd77b5163141fb025f8c in / 
# Tue, 23 May 2023 01:20:37 GMT
CMD ["bash"]
# Tue, 23 May 2023 08:26:56 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 08:27:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:27:21 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 08:27:21 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 08:27:24 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 08:27:24 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 08:27:24 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 08:27:27 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 08:27:27 GMT
ARG GHC=9.4.5
# Tue, 23 May 2023 08:27:27 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Tue, 23 May 2023 08:28:42 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.5 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='ecf16ec503e739e727174b29e5acbe4cf0c54737dd4d5eda046e09323f9ee248';             ;;         'x86_64')             GHC_SHA256='a44c39c4cc9a147de6dd31762995a9e47467cc91757800d80667b8cd60a9b226';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 08:28:47 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.5/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:28:47 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:99bf4787315b60d97d860ac6d006b7835b2241a601e93c2da4af6ca554be8704`  
		Last Modified: Tue, 23 May 2023 01:24:47 GMT  
		Size: 27.1 MB (27138577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922ab778f24e7006dd142f8df643984e8c1e678939e7104343f0975f2af889aa`  
		Last Modified: Tue, 23 May 2023 08:36:22 GMT  
		Size: 94.0 MB (94041102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af63a62ebad853e3687cdc43c53fa1acba67c351116e01715a614573acb3b5e`  
		Last Modified: Tue, 23 May 2023 08:36:11 GMT  
		Size: 13.7 MB (13736479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd32594f8ad3cb46719679dc1bec1d16f0fbd03b2fd29976b3b1c386f6e380f`  
		Last Modified: Tue, 23 May 2023 08:36:11 GMT  
		Size: 7.8 MB (7838380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7690bb755e90f1ef3becc286ac59274aaff9dd6ecf746fad997a95d14a3520b8`  
		Last Modified: Tue, 23 May 2023 08:36:54 GMT  
		Size: 269.3 MB (269271183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.4.5-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:99eb1374829355eb12431ea07110fa811c4f10a051b5ba43fbfe0eb574f296be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.5 MB (434516775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bbd3cd28aaae40586bf0407842546b69b3f5cc35e0ec70393550258dc83be95`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 00:43:28 GMT
ADD file:55a469039df0bf0e94ef7cd2d6fd355ad0c69e0e23e7921194445dd1fe281e3b in / 
# Tue, 23 May 2023 00:43:28 GMT
CMD ["bash"]
# Tue, 23 May 2023 02:13:23 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 02:13:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 02:13:42 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 02:13:42 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 02:13:50 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 02:13:51 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 02:13:51 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 02:13:53 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 02:13:53 GMT
ARG GHC=9.4.5
# Tue, 23 May 2023 02:13:53 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Tue, 23 May 2023 02:15:10 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.5 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='ecf16ec503e739e727174b29e5acbe4cf0c54737dd4d5eda046e09323f9ee248';             ;;         'x86_64')             GHC_SHA256='a44c39c4cc9a147de6dd31762995a9e47467cc91757800d80667b8cd60a9b226';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 02:15:22 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.5/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 02:15:22 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:3ca7b6c7180eac66b9c4301084a16319f41eb7f7365bdf91bcc272bd24cb4149`  
		Last Modified: Tue, 23 May 2023 00:46:44 GMT  
		Size: 25.9 MB (25921744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b1dfa9c7df4de9ed05420bd02fcbf79647f01f988f262f07cb0e1e6d68323d`  
		Last Modified: Tue, 23 May 2023 02:18:44 GMT  
		Size: 88.1 MB (88056276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87343452a5afdee6a1c296325e9b85c3424d00f396673e20fcab8554166166fe`  
		Last Modified: Tue, 23 May 2023 02:18:37 GMT  
		Size: 15.4 MB (15374105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba905b5698eb25fddd7444908f68d9b3bbe45263861f4c5346d9d95da1269fde`  
		Last Modified: Tue, 23 May 2023 02:18:37 GMT  
		Size: 12.4 MB (12373178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ff7a6c59b9c4ebd1c4fe70ce63a4eb0eaa932fa606622bf1fb0a68e6be1ea5`  
		Last Modified: Tue, 23 May 2023 02:19:15 GMT  
		Size: 292.8 MB (292791472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:buster`

```console
$ docker pull haskell@sha256:061a6d9588fc9fef00dc758428ee80db3e3d5c0b0b85666adefced246b7ab093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:buster` - linux; amd64

```console
$ docker pull haskell@sha256:e8609d28576e5715376ac4e4d12bc1a1680807c003e9b2f11b06a1c94312d193
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **721.3 MB (721262460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e0874f8537eeb3b079a734c33eafbf8ec0254c88e3e219bed678290e5d66d4`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 01:20:24 GMT
ADD file:9d769df745075dbc4cd2c01ca784571a0df008f6b650b895a7f92d3281132807 in / 
# Tue, 23 May 2023 01:20:25 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:50:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:50:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:52:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:25:03 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 08:25:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:25:08 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 08:25:08 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 08:25:11 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 08:25:11 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 08:25:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 08:25:14 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 08:25:14 GMT
ARG GHC=9.4.5
# Tue, 23 May 2023 08:25:14 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Tue, 23 May 2023 08:26:36 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.5 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='ecf16ec503e739e727174b29e5acbe4cf0c54737dd4d5eda046e09323f9ee248';             ;;         'x86_64')             GHC_SHA256='a44c39c4cc9a147de6dd31762995a9e47467cc91757800d80667b8cd60a9b226';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 08:26:43 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.5/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:26:43 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c722db24a050621ee87ea07acd5d066d3d6a94737c32012f27d73a1ad5cc645c`  
		Last Modified: Tue, 23 May 2023 01:24:26 GMT  
		Size: 50.4 MB (50448716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f8e4a0ed530ff1c74aea38be7ec6c725334c7c3a551b417d0f6f9e220a36fb`  
		Last Modified: Tue, 23 May 2023 01:57:08 GMT  
		Size: 17.6 MB (17580817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a739c67a76c3ff201aa979efc9c5deb081a75f5b98390ee176315cb0cb582aa9`  
		Last Modified: Tue, 23 May 2023 01:57:23 GMT  
		Size: 51.9 MB (51878369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e0d706266f768c6ed028e990dbb063fc43f6028827fe0f39ee6539a963e677`  
		Last Modified: Tue, 23 May 2023 01:57:52 GMT  
		Size: 191.9 MB (191886143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5899d9687951ca93548ece5e39287dc4f5b87d6733a2329490b95ac49b475905`  
		Last Modified: Tue, 23 May 2023 08:34:40 GMT  
		Size: 514.8 KB (514774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729ae0213f5e911798d1f7c2f3be7eaabda44bbf485853229978e6ea41918170`  
		Last Modified: Tue, 23 May 2023 08:34:42 GMT  
		Size: 13.7 MB (13736490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a49eb74c9b4a45e0eaf2f542af477fb0878c8110e8d36e175cb279b0e281636`  
		Last Modified: Tue, 23 May 2023 08:34:42 GMT  
		Size: 7.8 MB (7838367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55634913539c42cfcf42734839420cfb08b31a3ba2d1a174dd88894b1114e064`  
		Last Modified: Tue, 23 May 2023 08:35:46 GMT  
		Size: 387.4 MB (387378784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:c6ff674da0b5d75136bfad35ca6be581c583586625b0fc36f0a256ce0241ed62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **766.2 MB (766222838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77be8ca114cff75846de2efa9954abf091d4d3ac07a82c7d642595fa3f598b8`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 03 May 2023 00:22:56 GMT
ADD file:6042e29dcf5e22439cd69873d8960f8d3977abe915ef462aaa84368a7186a3bf in / 
# Wed, 03 May 2023 00:22:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:22:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:23:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:24:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 06:50:35 GMT
ENV LANG=C.UTF-8
# Thu, 04 May 2023 06:50:38 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 06:50:38 GMT
ARG STACK=2.9.3
# Thu, 04 May 2023 06:50:38 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 04 May 2023 06:50:42 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 04 May 2023 06:50:42 GMT
ARG CABAL_INSTALL=3.8.1.0
# Thu, 04 May 2023 06:50:42 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Thu, 04 May 2023 06:50:44 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 04 May 2023 06:50:44 GMT
ARG GHC=9.4.5
# Thu, 04 May 2023 06:50:44 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Thu, 04 May 2023 06:52:02 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.5 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='ecf16ec503e739e727174b29e5acbe4cf0c54737dd4d5eda046e09323f9ee248';             ;;         'x86_64')             GHC_SHA256='a44c39c4cc9a147de6dd31762995a9e47467cc91757800d80667b8cd60a9b226';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 04 May 2023 06:52:18 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.5/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 06:52:18 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b7c5fe8e0ac53c77142bf16686fc01d0d2b1fb2da7be5414cdf2f224ec485592`  
		Last Modified: Wed, 03 May 2023 00:26:10 GMT  
		Size: 49.2 MB (49238630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced623c8f9593ccbdc26a5e9ad9d9ad18aa6a8a3b82d7db591552673ac8e3281`  
		Last Modified: Wed, 03 May 2023 17:37:59 GMT  
		Size: 17.5 MB (17450341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fc649f7c89c148c32767dadfc283ae1472705773920b21ddd2bc77d49b2d64`  
		Last Modified: Wed, 03 May 2023 17:38:14 GMT  
		Size: 52.2 MB (52190435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7089b0cf38b0c4474188c7904744a3a55656697b95a3b5088cb510d0e932ba7`  
		Last Modified: Wed, 03 May 2023 17:38:38 GMT  
		Size: 183.5 MB (183454524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b29e6814a3ae5bdbc407544a41b3a6e63f55f582feff0b958bd39a45cac7ea`  
		Last Modified: Thu, 04 May 2023 06:55:45 GMT  
		Size: 517.0 KB (516952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a74f7761e2befcf0d84ef09bdf0daa0a7d4789a63da4f0384d3dc6a7246f1cc`  
		Last Modified: Thu, 04 May 2023 06:55:47 GMT  
		Size: 15.4 MB (15374096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108ebc522e506a00d8bd87318b5a587329490286725a8267770ee95b0caf2273`  
		Last Modified: Thu, 04 May 2023 06:55:47 GMT  
		Size: 12.4 MB (12373196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff3ed3db5bee2805f9b104d9e3c2ce074ec04bdd666c74d543802081ed6c5f6`  
		Last Modified: Thu, 04 May 2023 06:56:48 GMT  
		Size: 435.6 MB (435624664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:latest`

```console
$ docker pull haskell@sha256:061a6d9588fc9fef00dc758428ee80db3e3d5c0b0b85666adefced246b7ab093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:latest` - linux; amd64

```console
$ docker pull haskell@sha256:e8609d28576e5715376ac4e4d12bc1a1680807c003e9b2f11b06a1c94312d193
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **721.3 MB (721262460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e0874f8537eeb3b079a734c33eafbf8ec0254c88e3e219bed678290e5d66d4`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 01:20:24 GMT
ADD file:9d769df745075dbc4cd2c01ca784571a0df008f6b650b895a7f92d3281132807 in / 
# Tue, 23 May 2023 01:20:25 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:50:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:50:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:52:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:25:03 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 08:25:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:25:08 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 08:25:08 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 08:25:11 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 08:25:11 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 08:25:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 08:25:14 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 08:25:14 GMT
ARG GHC=9.4.5
# Tue, 23 May 2023 08:25:14 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Tue, 23 May 2023 08:26:36 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.5 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='ecf16ec503e739e727174b29e5acbe4cf0c54737dd4d5eda046e09323f9ee248';             ;;         'x86_64')             GHC_SHA256='a44c39c4cc9a147de6dd31762995a9e47467cc91757800d80667b8cd60a9b226';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 08:26:43 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.5/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:26:43 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c722db24a050621ee87ea07acd5d066d3d6a94737c32012f27d73a1ad5cc645c`  
		Last Modified: Tue, 23 May 2023 01:24:26 GMT  
		Size: 50.4 MB (50448716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f8e4a0ed530ff1c74aea38be7ec6c725334c7c3a551b417d0f6f9e220a36fb`  
		Last Modified: Tue, 23 May 2023 01:57:08 GMT  
		Size: 17.6 MB (17580817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a739c67a76c3ff201aa979efc9c5deb081a75f5b98390ee176315cb0cb582aa9`  
		Last Modified: Tue, 23 May 2023 01:57:23 GMT  
		Size: 51.9 MB (51878369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e0d706266f768c6ed028e990dbb063fc43f6028827fe0f39ee6539a963e677`  
		Last Modified: Tue, 23 May 2023 01:57:52 GMT  
		Size: 191.9 MB (191886143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5899d9687951ca93548ece5e39287dc4f5b87d6733a2329490b95ac49b475905`  
		Last Modified: Tue, 23 May 2023 08:34:40 GMT  
		Size: 514.8 KB (514774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729ae0213f5e911798d1f7c2f3be7eaabda44bbf485853229978e6ea41918170`  
		Last Modified: Tue, 23 May 2023 08:34:42 GMT  
		Size: 13.7 MB (13736490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a49eb74c9b4a45e0eaf2f542af477fb0878c8110e8d36e175cb279b0e281636`  
		Last Modified: Tue, 23 May 2023 08:34:42 GMT  
		Size: 7.8 MB (7838367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55634913539c42cfcf42734839420cfb08b31a3ba2d1a174dd88894b1114e064`  
		Last Modified: Tue, 23 May 2023 08:35:46 GMT  
		Size: 387.4 MB (387378784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:latest` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:c6ff674da0b5d75136bfad35ca6be581c583586625b0fc36f0a256ce0241ed62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **766.2 MB (766222838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77be8ca114cff75846de2efa9954abf091d4d3ac07a82c7d642595fa3f598b8`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 03 May 2023 00:22:56 GMT
ADD file:6042e29dcf5e22439cd69873d8960f8d3977abe915ef462aaa84368a7186a3bf in / 
# Wed, 03 May 2023 00:22:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:22:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:23:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:24:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 06:50:35 GMT
ENV LANG=C.UTF-8
# Thu, 04 May 2023 06:50:38 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 06:50:38 GMT
ARG STACK=2.9.3
# Thu, 04 May 2023 06:50:38 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 04 May 2023 06:50:42 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 04 May 2023 06:50:42 GMT
ARG CABAL_INSTALL=3.8.1.0
# Thu, 04 May 2023 06:50:42 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Thu, 04 May 2023 06:50:44 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 04 May 2023 06:50:44 GMT
ARG GHC=9.4.5
# Thu, 04 May 2023 06:50:44 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Thu, 04 May 2023 06:52:02 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.5 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='ecf16ec503e739e727174b29e5acbe4cf0c54737dd4d5eda046e09323f9ee248';             ;;         'x86_64')             GHC_SHA256='a44c39c4cc9a147de6dd31762995a9e47467cc91757800d80667b8cd60a9b226';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 04 May 2023 06:52:18 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.5/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 06:52:18 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b7c5fe8e0ac53c77142bf16686fc01d0d2b1fb2da7be5414cdf2f224ec485592`  
		Last Modified: Wed, 03 May 2023 00:26:10 GMT  
		Size: 49.2 MB (49238630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced623c8f9593ccbdc26a5e9ad9d9ad18aa6a8a3b82d7db591552673ac8e3281`  
		Last Modified: Wed, 03 May 2023 17:37:59 GMT  
		Size: 17.5 MB (17450341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fc649f7c89c148c32767dadfc283ae1472705773920b21ddd2bc77d49b2d64`  
		Last Modified: Wed, 03 May 2023 17:38:14 GMT  
		Size: 52.2 MB (52190435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7089b0cf38b0c4474188c7904744a3a55656697b95a3b5088cb510d0e932ba7`  
		Last Modified: Wed, 03 May 2023 17:38:38 GMT  
		Size: 183.5 MB (183454524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b29e6814a3ae5bdbc407544a41b3a6e63f55f582feff0b958bd39a45cac7ea`  
		Last Modified: Thu, 04 May 2023 06:55:45 GMT  
		Size: 517.0 KB (516952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a74f7761e2befcf0d84ef09bdf0daa0a7d4789a63da4f0384d3dc6a7246f1cc`  
		Last Modified: Thu, 04 May 2023 06:55:47 GMT  
		Size: 15.4 MB (15374096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108ebc522e506a00d8bd87318b5a587329490286725a8267770ee95b0caf2273`  
		Last Modified: Thu, 04 May 2023 06:55:47 GMT  
		Size: 12.4 MB (12373196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff3ed3db5bee2805f9b104d9e3c2ce074ec04bdd666c74d543802081ed6c5f6`  
		Last Modified: Thu, 04 May 2023 06:56:48 GMT  
		Size: 435.6 MB (435624664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:slim`

```console
$ docker pull haskell@sha256:77551349dce35ba3f6f95ad53d736e261ab59b467a3af4164b5bfa51ccebfcce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:slim` - linux; amd64

```console
$ docker pull haskell@sha256:89fb63973f87062b26c1cab096f57c5b22b59473ba47f66389ad7ca078e706f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.0 MB (412025721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd594b4728b6f2ba7bb38f2fb399469ef9007208631c554c3e8f71b6f4eda081`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 01:20:37 GMT
ADD file:2058e04b33179527a56999678c1c62dfcf76944675afcd77b5163141fb025f8c in / 
# Tue, 23 May 2023 01:20:37 GMT
CMD ["bash"]
# Tue, 23 May 2023 08:26:56 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 08:27:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:27:21 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 08:27:21 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 08:27:24 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 08:27:24 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 08:27:24 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 08:27:27 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 08:27:27 GMT
ARG GHC=9.4.5
# Tue, 23 May 2023 08:27:27 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Tue, 23 May 2023 08:28:42 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.5 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='ecf16ec503e739e727174b29e5acbe4cf0c54737dd4d5eda046e09323f9ee248';             ;;         'x86_64')             GHC_SHA256='a44c39c4cc9a147de6dd31762995a9e47467cc91757800d80667b8cd60a9b226';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 08:28:47 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.5/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:28:47 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:99bf4787315b60d97d860ac6d006b7835b2241a601e93c2da4af6ca554be8704`  
		Last Modified: Tue, 23 May 2023 01:24:47 GMT  
		Size: 27.1 MB (27138577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922ab778f24e7006dd142f8df643984e8c1e678939e7104343f0975f2af889aa`  
		Last Modified: Tue, 23 May 2023 08:36:22 GMT  
		Size: 94.0 MB (94041102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af63a62ebad853e3687cdc43c53fa1acba67c351116e01715a614573acb3b5e`  
		Last Modified: Tue, 23 May 2023 08:36:11 GMT  
		Size: 13.7 MB (13736479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd32594f8ad3cb46719679dc1bec1d16f0fbd03b2fd29976b3b1c386f6e380f`  
		Last Modified: Tue, 23 May 2023 08:36:11 GMT  
		Size: 7.8 MB (7838380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7690bb755e90f1ef3becc286ac59274aaff9dd6ecf746fad997a95d14a3520b8`  
		Last Modified: Tue, 23 May 2023 08:36:54 GMT  
		Size: 269.3 MB (269271183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:99eb1374829355eb12431ea07110fa811c4f10a051b5ba43fbfe0eb574f296be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.5 MB (434516775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bbd3cd28aaae40586bf0407842546b69b3f5cc35e0ec70393550258dc83be95`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 00:43:28 GMT
ADD file:55a469039df0bf0e94ef7cd2d6fd355ad0c69e0e23e7921194445dd1fe281e3b in / 
# Tue, 23 May 2023 00:43:28 GMT
CMD ["bash"]
# Tue, 23 May 2023 02:13:23 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 02:13:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 02:13:42 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 02:13:42 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 02:13:50 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 02:13:51 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 02:13:51 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 02:13:53 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 02:13:53 GMT
ARG GHC=9.4.5
# Tue, 23 May 2023 02:13:53 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Tue, 23 May 2023 02:15:10 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.5 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='ecf16ec503e739e727174b29e5acbe4cf0c54737dd4d5eda046e09323f9ee248';             ;;         'x86_64')             GHC_SHA256='a44c39c4cc9a147de6dd31762995a9e47467cc91757800d80667b8cd60a9b226';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 02:15:22 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.5/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 02:15:22 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:3ca7b6c7180eac66b9c4301084a16319f41eb7f7365bdf91bcc272bd24cb4149`  
		Last Modified: Tue, 23 May 2023 00:46:44 GMT  
		Size: 25.9 MB (25921744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b1dfa9c7df4de9ed05420bd02fcbf79647f01f988f262f07cb0e1e6d68323d`  
		Last Modified: Tue, 23 May 2023 02:18:44 GMT  
		Size: 88.1 MB (88056276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87343452a5afdee6a1c296325e9b85c3424d00f396673e20fcab8554166166fe`  
		Last Modified: Tue, 23 May 2023 02:18:37 GMT  
		Size: 15.4 MB (15374105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba905b5698eb25fddd7444908f68d9b3bbe45263861f4c5346d9d95da1269fde`  
		Last Modified: Tue, 23 May 2023 02:18:37 GMT  
		Size: 12.4 MB (12373178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ff7a6c59b9c4ebd1c4fe70ce63a4eb0eaa932fa606622bf1fb0a68e6be1ea5`  
		Last Modified: Tue, 23 May 2023 02:19:15 GMT  
		Size: 292.8 MB (292791472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:slim-buster`

```console
$ docker pull haskell@sha256:77551349dce35ba3f6f95ad53d736e261ab59b467a3af4164b5bfa51ccebfcce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:89fb63973f87062b26c1cab096f57c5b22b59473ba47f66389ad7ca078e706f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.0 MB (412025721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd594b4728b6f2ba7bb38f2fb399469ef9007208631c554c3e8f71b6f4eda081`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 01:20:37 GMT
ADD file:2058e04b33179527a56999678c1c62dfcf76944675afcd77b5163141fb025f8c in / 
# Tue, 23 May 2023 01:20:37 GMT
CMD ["bash"]
# Tue, 23 May 2023 08:26:56 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 08:27:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 08:27:21 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 08:27:21 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 08:27:24 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 08:27:24 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 08:27:24 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 08:27:27 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 08:27:27 GMT
ARG GHC=9.4.5
# Tue, 23 May 2023 08:27:27 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Tue, 23 May 2023 08:28:42 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.5 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='ecf16ec503e739e727174b29e5acbe4cf0c54737dd4d5eda046e09323f9ee248';             ;;         'x86_64')             GHC_SHA256='a44c39c4cc9a147de6dd31762995a9e47467cc91757800d80667b8cd60a9b226';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 08:28:47 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.5/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:28:47 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:99bf4787315b60d97d860ac6d006b7835b2241a601e93c2da4af6ca554be8704`  
		Last Modified: Tue, 23 May 2023 01:24:47 GMT  
		Size: 27.1 MB (27138577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922ab778f24e7006dd142f8df643984e8c1e678939e7104343f0975f2af889aa`  
		Last Modified: Tue, 23 May 2023 08:36:22 GMT  
		Size: 94.0 MB (94041102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af63a62ebad853e3687cdc43c53fa1acba67c351116e01715a614573acb3b5e`  
		Last Modified: Tue, 23 May 2023 08:36:11 GMT  
		Size: 13.7 MB (13736479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd32594f8ad3cb46719679dc1bec1d16f0fbd03b2fd29976b3b1c386f6e380f`  
		Last Modified: Tue, 23 May 2023 08:36:11 GMT  
		Size: 7.8 MB (7838380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7690bb755e90f1ef3becc286ac59274aaff9dd6ecf746fad997a95d14a3520b8`  
		Last Modified: Tue, 23 May 2023 08:36:54 GMT  
		Size: 269.3 MB (269271183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:99eb1374829355eb12431ea07110fa811c4f10a051b5ba43fbfe0eb574f296be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.5 MB (434516775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bbd3cd28aaae40586bf0407842546b69b3f5cc35e0ec70393550258dc83be95`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 May 2023 00:43:28 GMT
ADD file:55a469039df0bf0e94ef7cd2d6fd355ad0c69e0e23e7921194445dd1fe281e3b in / 
# Tue, 23 May 2023 00:43:28 GMT
CMD ["bash"]
# Tue, 23 May 2023 02:13:23 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 02:13:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 02:13:42 GMT
ARG STACK=2.9.3
# Tue, 23 May 2023 02:13:42 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 23 May 2023 02:13:50 GMT
# ARGS: STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='161e1638da9efc56319f7225b3652ca3f339bcda9eadc7d6ce512f325b0f014a';             ;;         'x86_64')             STACK_SHA256='938f689dc45e2693ab1ca3ea215790b3786dfd531dcf6c0bf40842c24e579ae9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 23 May 2023 02:13:51 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 23 May 2023 02:13:51 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 23 May 2023 02:13:53 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 23 May 2023 02:13:53 GMT
ARG GHC=9.4.5
# Tue, 23 May 2023 02:13:53 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Tue, 23 May 2023 02:15:10 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.5 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.9.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='ecf16ec503e739e727174b29e5acbe4cf0c54737dd4d5eda046e09323f9ee248';             ;;         'x86_64')             GHC_SHA256='a44c39c4cc9a147de6dd31762995a9e47467cc91757800d80667b8cd60a9b226';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 23 May 2023 02:15:22 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.5/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 02:15:22 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:3ca7b6c7180eac66b9c4301084a16319f41eb7f7365bdf91bcc272bd24cb4149`  
		Last Modified: Tue, 23 May 2023 00:46:44 GMT  
		Size: 25.9 MB (25921744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b1dfa9c7df4de9ed05420bd02fcbf79647f01f988f262f07cb0e1e6d68323d`  
		Last Modified: Tue, 23 May 2023 02:18:44 GMT  
		Size: 88.1 MB (88056276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87343452a5afdee6a1c296325e9b85c3424d00f396673e20fcab8554166166fe`  
		Last Modified: Tue, 23 May 2023 02:18:37 GMT  
		Size: 15.4 MB (15374105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba905b5698eb25fddd7444908f68d9b3bbe45263861f4c5346d9d95da1269fde`  
		Last Modified: Tue, 23 May 2023 02:18:37 GMT  
		Size: 12.4 MB (12373178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ff7a6c59b9c4ebd1c4fe70ce63a4eb0eaa932fa606622bf1fb0a68e6be1ea5`  
		Last Modified: Tue, 23 May 2023 02:19:15 GMT  
		Size: 292.8 MB (292791472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
