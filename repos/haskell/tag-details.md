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
-	[`haskell:9.2.8`](#haskell928)
-	[`haskell:9.2.8-buster`](#haskell928-buster)
-	[`haskell:9.2.8-slim`](#haskell928-slim)
-	[`haskell:9.2.8-slim-buster`](#haskell928-slim-buster)
-	[`haskell:9.4`](#haskell94)
-	[`haskell:9.4-buster`](#haskell94-buster)
-	[`haskell:9.4-slim`](#haskell94-slim)
-	[`haskell:9.4-slim-buster`](#haskell94-slim-buster)
-	[`haskell:9.4.8`](#haskell948)
-	[`haskell:9.4.8-buster`](#haskell948-buster)
-	[`haskell:9.4.8-slim`](#haskell948-slim)
-	[`haskell:9.4.8-slim-buster`](#haskell948-slim-buster)
-	[`haskell:9.6`](#haskell96)
-	[`haskell:9.6-buster`](#haskell96-buster)
-	[`haskell:9.6-slim`](#haskell96-slim)
-	[`haskell:9.6-slim-buster`](#haskell96-slim-buster)
-	[`haskell:9.6.3`](#haskell963)
-	[`haskell:9.6.3-buster`](#haskell963-buster)
-	[`haskell:9.6.3-slim`](#haskell963-slim)
-	[`haskell:9.6.3-slim-buster`](#haskell963-slim-buster)
-	[`haskell:9.8`](#haskell98)
-	[`haskell:9.8-buster`](#haskell98-buster)
-	[`haskell:9.8-slim`](#haskell98-slim)
-	[`haskell:9.8-slim-buster`](#haskell98-slim-buster)
-	[`haskell:9.8.1`](#haskell981)
-	[`haskell:9.8.1-buster`](#haskell981-buster)
-	[`haskell:9.8.1-slim`](#haskell981-slim)
-	[`haskell:9.8.1-slim-buster`](#haskell981-slim-buster)
-	[`haskell:buster`](#haskellbuster)
-	[`haskell:latest`](#haskelllatest)
-	[`haskell:slim`](#haskellslim)
-	[`haskell:slim-buster`](#haskellslim-buster)

## `haskell:9`

```console
$ docker pull haskell@sha256:0d951e083ab7089d8de9ec0e5eb142eaefd70ec6b1de7d5da8a38d16afec38f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9` - linux; amd64

```console
$ docker pull haskell@sha256:4980ba75628c7718b4c9b6745f4f89f8ddd9f34dca6c99e44e68d78f126c23e8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.4 MB (776377925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b5ce25e74c90a93b499beec7d97268d61bc3f9de57eb375165b09043fdbd9a`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:08 GMT
ADD file:4f8b7a35280160ec5a55323fa07ac91e294c86e2ea647ba212053983ef380bcf in / 
# Tue, 21 Nov 2023 05:22:08 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:55:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:56:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:57:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:47 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:39:51 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:39:55 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:39:58 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:39:58 GMT
ARG GHC=9.8.1
# Tue, 21 Nov 2023 12:39:58 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 21 Nov 2023 12:41:39 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.8.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='aab7af72614f8bf9ca624407aa4dbc69bc009c2b4cc1a0f3c062008db81bdb95';             ;;         'x86_64')             GHC_SHA256='d498657ca00514bc4620b591f74b93f9a3b64e5282e5c4e2876a734c130f1fbf';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:41:46 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:41:46 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b32028968d56a86ac35eac062e7abba276c547ab175fb057973c469eb41db55b`  
		Last Modified: Tue, 21 Nov 2023 05:26:57 GMT  
		Size: 50.5 MB (50499471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24c059838ae87ccefc35d50177e4e280a9e6f2f54127456ad0eaa5be5ed5386`  
		Last Modified: Tue, 21 Nov 2023 10:03:28 GMT  
		Size: 17.6 MB (17583860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819458a39dea8d30616a22068e79bcb7743745aa8b0d35fdb762ba69d98e3ec0`  
		Last Modified: Tue, 21 Nov 2023 10:03:45 GMT  
		Size: 51.9 MB (51874180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedd23d9034d9de62653c3bb2a2ca71fb88a1c6d17f386c0bfe4ac5bf8163929`  
		Last Modified: Tue, 21 Nov 2023 10:04:21 GMT  
		Size: 191.9 MB (191910019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ef9a56930d28877c2fa90904a7be44f1f8cca3356383b7f74682c75d8d994`  
		Last Modified: Tue, 21 Nov 2023 12:57:42 GMT  
		Size: 515.2 KB (515154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a1f56bfe415e8ae3055b472ce7df60a5bdf1033339c4dd235e31d400eb34c3`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 15.4 MB (15359949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35eecb76c7d0d3257ad0d1322fa0f70fe5bb08f73cd35791e40dedfeb7df855e`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8af2da252abb99a9c81a472596ee087886baad4962118fe1d876c34e7411515`  
		Last Modified: Tue, 21 Nov 2023 12:58:59 GMT  
		Size: 440.8 MB (440796924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:fbcca4aa25ce81d1ab6394e57ee65731ac1db80da098f4bbb596c2dea45e5535
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **781.9 MB (781863866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eeee2b51045fdea358f3b07474255e2fde2ecbb95984cec270e3b99fc72e262`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:27 GMT
ADD file:ea38b381ee92d0c4b34697af5b78def83b881e6837b309e1f41a14bee2ff2b7e in / 
# Tue, 21 Nov 2023 06:27:27 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:00:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:00:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:01:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:18 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 08:21:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 08:21:25 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 08:21:28 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 08:21:28 GMT
ARG GHC=9.8.1
# Tue, 21 Nov 2023 08:21:28 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 21 Nov 2023 08:23:06 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.8.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='aab7af72614f8bf9ca624407aa4dbc69bc009c2b4cc1a0f3c062008db81bdb95';             ;;         'x86_64')             GHC_SHA256='d498657ca00514bc4620b591f74b93f9a3b64e5282e5c4e2876a734c130f1fbf';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 08:23:18 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 08:23:19 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:357c576c57e480da5e7eb018506db51d822da9f357c02a76f7c4da1ccaa61b33`  
		Last Modified: Tue, 21 Nov 2023 06:31:24 GMT  
		Size: 49.3 MB (49291145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9750a1d4e9cc8d118fb8f247658f2e931026ab641d4ebdc3c3806b3dd8ee4d0d`  
		Last Modified: Tue, 21 Nov 2023 08:07:51 GMT  
		Size: 17.5 MB (17454097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55295586deeb07a4153f5f4d0cd2723a2240e52697d6ad85612c498057c0d832`  
		Last Modified: Tue, 21 Nov 2023 08:08:06 GMT  
		Size: 52.2 MB (52207152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fb9e461a1bbc28daea6d98c6425175d5ec238091b9c6d22306c3d257de50cd`  
		Last Modified: Tue, 21 Nov 2023 08:08:31 GMT  
		Size: 183.5 MB (183476090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8520593e4d4d8289c877a174b696c2830f14eb2b1b3a3a832ad50cb64aa23049`  
		Last Modified: Tue, 21 Nov 2023 08:39:07 GMT  
		Size: 517.3 KB (517300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234bbe5f5278dc328477465898a776d8addb6172cfc0ae55d199f015a74987c`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 17.2 MB (17230042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ed20186e4d0efa5eec675e66c421203c5fe383a529511ab58816cb659b96a0`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 12.4 MB (12373189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43422b7863f897378a29540b4f90bb753c6f1bf0e4988c233e62989f587e6ad8`  
		Last Modified: Tue, 21 Nov 2023 08:40:14 GMT  
		Size: 449.3 MB (449314851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9-buster`

```console
$ docker pull haskell@sha256:0d951e083ab7089d8de9ec0e5eb142eaefd70ec6b1de7d5da8a38d16afec38f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9-buster` - linux; amd64

```console
$ docker pull haskell@sha256:4980ba75628c7718b4c9b6745f4f89f8ddd9f34dca6c99e44e68d78f126c23e8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.4 MB (776377925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b5ce25e74c90a93b499beec7d97268d61bc3f9de57eb375165b09043fdbd9a`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:08 GMT
ADD file:4f8b7a35280160ec5a55323fa07ac91e294c86e2ea647ba212053983ef380bcf in / 
# Tue, 21 Nov 2023 05:22:08 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:55:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:56:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:57:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:47 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:39:51 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:39:55 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:39:58 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:39:58 GMT
ARG GHC=9.8.1
# Tue, 21 Nov 2023 12:39:58 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 21 Nov 2023 12:41:39 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.8.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='aab7af72614f8bf9ca624407aa4dbc69bc009c2b4cc1a0f3c062008db81bdb95';             ;;         'x86_64')             GHC_SHA256='d498657ca00514bc4620b591f74b93f9a3b64e5282e5c4e2876a734c130f1fbf';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:41:46 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:41:46 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b32028968d56a86ac35eac062e7abba276c547ab175fb057973c469eb41db55b`  
		Last Modified: Tue, 21 Nov 2023 05:26:57 GMT  
		Size: 50.5 MB (50499471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24c059838ae87ccefc35d50177e4e280a9e6f2f54127456ad0eaa5be5ed5386`  
		Last Modified: Tue, 21 Nov 2023 10:03:28 GMT  
		Size: 17.6 MB (17583860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819458a39dea8d30616a22068e79bcb7743745aa8b0d35fdb762ba69d98e3ec0`  
		Last Modified: Tue, 21 Nov 2023 10:03:45 GMT  
		Size: 51.9 MB (51874180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedd23d9034d9de62653c3bb2a2ca71fb88a1c6d17f386c0bfe4ac5bf8163929`  
		Last Modified: Tue, 21 Nov 2023 10:04:21 GMT  
		Size: 191.9 MB (191910019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ef9a56930d28877c2fa90904a7be44f1f8cca3356383b7f74682c75d8d994`  
		Last Modified: Tue, 21 Nov 2023 12:57:42 GMT  
		Size: 515.2 KB (515154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a1f56bfe415e8ae3055b472ce7df60a5bdf1033339c4dd235e31d400eb34c3`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 15.4 MB (15359949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35eecb76c7d0d3257ad0d1322fa0f70fe5bb08f73cd35791e40dedfeb7df855e`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8af2da252abb99a9c81a472596ee087886baad4962118fe1d876c34e7411515`  
		Last Modified: Tue, 21 Nov 2023 12:58:59 GMT  
		Size: 440.8 MB (440796924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:fbcca4aa25ce81d1ab6394e57ee65731ac1db80da098f4bbb596c2dea45e5535
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **781.9 MB (781863866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eeee2b51045fdea358f3b07474255e2fde2ecbb95984cec270e3b99fc72e262`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:27 GMT
ADD file:ea38b381ee92d0c4b34697af5b78def83b881e6837b309e1f41a14bee2ff2b7e in / 
# Tue, 21 Nov 2023 06:27:27 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:00:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:00:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:01:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:18 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 08:21:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 08:21:25 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 08:21:28 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 08:21:28 GMT
ARG GHC=9.8.1
# Tue, 21 Nov 2023 08:21:28 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 21 Nov 2023 08:23:06 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.8.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='aab7af72614f8bf9ca624407aa4dbc69bc009c2b4cc1a0f3c062008db81bdb95';             ;;         'x86_64')             GHC_SHA256='d498657ca00514bc4620b591f74b93f9a3b64e5282e5c4e2876a734c130f1fbf';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 08:23:18 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 08:23:19 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:357c576c57e480da5e7eb018506db51d822da9f357c02a76f7c4da1ccaa61b33`  
		Last Modified: Tue, 21 Nov 2023 06:31:24 GMT  
		Size: 49.3 MB (49291145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9750a1d4e9cc8d118fb8f247658f2e931026ab641d4ebdc3c3806b3dd8ee4d0d`  
		Last Modified: Tue, 21 Nov 2023 08:07:51 GMT  
		Size: 17.5 MB (17454097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55295586deeb07a4153f5f4d0cd2723a2240e52697d6ad85612c498057c0d832`  
		Last Modified: Tue, 21 Nov 2023 08:08:06 GMT  
		Size: 52.2 MB (52207152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fb9e461a1bbc28daea6d98c6425175d5ec238091b9c6d22306c3d257de50cd`  
		Last Modified: Tue, 21 Nov 2023 08:08:31 GMT  
		Size: 183.5 MB (183476090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8520593e4d4d8289c877a174b696c2830f14eb2b1b3a3a832ad50cb64aa23049`  
		Last Modified: Tue, 21 Nov 2023 08:39:07 GMT  
		Size: 517.3 KB (517300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234bbe5f5278dc328477465898a776d8addb6172cfc0ae55d199f015a74987c`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 17.2 MB (17230042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ed20186e4d0efa5eec675e66c421203c5fe383a529511ab58816cb659b96a0`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 12.4 MB (12373189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43422b7863f897378a29540b4f90bb753c6f1bf0e4988c233e62989f587e6ad8`  
		Last Modified: Tue, 21 Nov 2023 08:40:14 GMT  
		Size: 449.3 MB (449314851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9-slim`

```console
$ docker pull haskell@sha256:29baea3db36c4a985f95bb1a4530d43073278ea4103a10a5dc968254d94b235d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9-slim` - linux; amd64

```console
$ docker pull haskell@sha256:858b76cb891a02f4ced5fd2c2626cc26fd6a6f1054f2dcc05647729a214a50b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.6 MB (440611509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82237bb5b6bc25c2590d0feecb0b38ddc2420c9a9dbf5449f3b99cc3e357e3f2`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:20 GMT
ADD file:7672eb709be933bb0edec47b8141cd2ebff266a770dfae1278205f7cee43c71a in / 
# Tue, 21 Nov 2023 05:22:20 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:41:56 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:42:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:42:21 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:42:24 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:42:24 GMT
ARG GHC=9.8.1
# Tue, 21 Nov 2023 12:42:24 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 21 Nov 2023 12:43:59 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.8.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='aab7af72614f8bf9ca624407aa4dbc69bc009c2b4cc1a0f3c062008db81bdb95';             ;;         'x86_64')             GHC_SHA256='d498657ca00514bc4620b591f74b93f9a3b64e5282e5c4e2876a734c130f1fbf';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:44:05 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:44:05 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0fc9206bc4affb32fe13185a20b8184271c753e9b7cb81484bf770054fc69737`  
		Last Modified: Tue, 21 Nov 2023 05:27:19 GMT  
		Size: 27.2 MB (27187457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6213b4299e71dcc2c16c339ec043da12cc47384caa53a9f15259996652e6bf4`  
		Last Modified: Tue, 21 Nov 2023 12:59:36 GMT  
		Size: 94.0 MB (94045021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19344eacbd857e0b61cb66092db6d11c467aed149978f45a1dcdb057ebb9980`  
		Last Modified: Tue, 21 Nov 2023 12:59:24 GMT  
		Size: 15.4 MB (15359960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefb56630c3948901bac3dd75868f7d017f4b46579498b8fdf054347f3db9894`  
		Last Modified: Tue, 21 Nov 2023 12:59:23 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691c29c1b65c9a94e88a29baf35e37dc0dc3f7e5e2228ad58480cced1a0de925`  
		Last Modified: Tue, 21 Nov 2023 13:00:14 GMT  
		Size: 296.2 MB (296180703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:8fb474264853e6be6007319bf8e2bd44475878d391bfaa4a5514db11f7b9c9cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.5 MB (447484012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe30b2fc483028ca9f909ab40fd8c7add1905982844b35d0ff95e3c274fad370`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:39 GMT
ADD file:f60673c303a98b4e4c676e3403bc1b7cb316335aba1202205188176810494c07 in / 
# Tue, 19 Dec 2023 01:41:40 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:46:03 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 02:46:21 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK=2.11.1
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 19 Dec 2023 02:46:31 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 19 Dec 2023 02:46:34 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 19 Dec 2023 02:46:34 GMT
ARG GHC=9.8.1
# Tue, 19 Dec 2023 02:46:34 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 19 Dec 2023 02:48:05 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.8.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='aab7af72614f8bf9ca624407aa4dbc69bc009c2b4cc1a0f3c062008db81bdb95';             ;;         'x86_64')             GHC_SHA256='d498657ca00514bc4620b591f74b93f9a3b64e5282e5c4e2876a734c130f1fbf';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 19 Dec 2023 02:48:16 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 02:48:17 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c0b0171eefd1c6d7f85c54d4a609269c9b5e19a0fd8cd787a49c808c6b73cf74`  
		Last Modified: Tue, 19 Dec 2023 01:46:01 GMT  
		Size: 26.0 MB (25969827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6ed82599775f9bbd4cc3c5df2ebf7342daaa490b970568c1ea375e3242ebc4`  
		Last Modified: Tue, 19 Dec 2023 02:55:11 GMT  
		Size: 88.1 MB (88053431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a99edfe152899f2001989c0e6103ad6f2276cf961df3dbb4aceefec5312d373`  
		Last Modified: Tue, 19 Dec 2023 02:55:02 GMT  
		Size: 17.2 MB (17230056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20252565f8094ddee6562ad5f30ebc81e720ba92b526c0174372c3fad25e8625`  
		Last Modified: Tue, 19 Dec 2023 02:55:01 GMT  
		Size: 12.4 MB (12373194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df373a3b6f590305ac40bf712eb84f342145370ea6225181d41b1fe3229f6178`  
		Last Modified: Tue, 19 Dec 2023 02:55:44 GMT  
		Size: 303.9 MB (303857504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9-slim-buster`

```console
$ docker pull haskell@sha256:29baea3db36c4a985f95bb1a4530d43073278ea4103a10a5dc968254d94b235d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:858b76cb891a02f4ced5fd2c2626cc26fd6a6f1054f2dcc05647729a214a50b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.6 MB (440611509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82237bb5b6bc25c2590d0feecb0b38ddc2420c9a9dbf5449f3b99cc3e357e3f2`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:20 GMT
ADD file:7672eb709be933bb0edec47b8141cd2ebff266a770dfae1278205f7cee43c71a in / 
# Tue, 21 Nov 2023 05:22:20 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:41:56 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:42:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:42:21 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:42:24 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:42:24 GMT
ARG GHC=9.8.1
# Tue, 21 Nov 2023 12:42:24 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 21 Nov 2023 12:43:59 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.8.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='aab7af72614f8bf9ca624407aa4dbc69bc009c2b4cc1a0f3c062008db81bdb95';             ;;         'x86_64')             GHC_SHA256='d498657ca00514bc4620b591f74b93f9a3b64e5282e5c4e2876a734c130f1fbf';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:44:05 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:44:05 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0fc9206bc4affb32fe13185a20b8184271c753e9b7cb81484bf770054fc69737`  
		Last Modified: Tue, 21 Nov 2023 05:27:19 GMT  
		Size: 27.2 MB (27187457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6213b4299e71dcc2c16c339ec043da12cc47384caa53a9f15259996652e6bf4`  
		Last Modified: Tue, 21 Nov 2023 12:59:36 GMT  
		Size: 94.0 MB (94045021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19344eacbd857e0b61cb66092db6d11c467aed149978f45a1dcdb057ebb9980`  
		Last Modified: Tue, 21 Nov 2023 12:59:24 GMT  
		Size: 15.4 MB (15359960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefb56630c3948901bac3dd75868f7d017f4b46579498b8fdf054347f3db9894`  
		Last Modified: Tue, 21 Nov 2023 12:59:23 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691c29c1b65c9a94e88a29baf35e37dc0dc3f7e5e2228ad58480cced1a0de925`  
		Last Modified: Tue, 21 Nov 2023 13:00:14 GMT  
		Size: 296.2 MB (296180703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:8fb474264853e6be6007319bf8e2bd44475878d391bfaa4a5514db11f7b9c9cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.5 MB (447484012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe30b2fc483028ca9f909ab40fd8c7add1905982844b35d0ff95e3c274fad370`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:39 GMT
ADD file:f60673c303a98b4e4c676e3403bc1b7cb316335aba1202205188176810494c07 in / 
# Tue, 19 Dec 2023 01:41:40 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:46:03 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 02:46:21 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK=2.11.1
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 19 Dec 2023 02:46:31 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 19 Dec 2023 02:46:34 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 19 Dec 2023 02:46:34 GMT
ARG GHC=9.8.1
# Tue, 19 Dec 2023 02:46:34 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 19 Dec 2023 02:48:05 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.8.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='aab7af72614f8bf9ca624407aa4dbc69bc009c2b4cc1a0f3c062008db81bdb95';             ;;         'x86_64')             GHC_SHA256='d498657ca00514bc4620b591f74b93f9a3b64e5282e5c4e2876a734c130f1fbf';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 19 Dec 2023 02:48:16 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 02:48:17 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c0b0171eefd1c6d7f85c54d4a609269c9b5e19a0fd8cd787a49c808c6b73cf74`  
		Last Modified: Tue, 19 Dec 2023 01:46:01 GMT  
		Size: 26.0 MB (25969827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6ed82599775f9bbd4cc3c5df2ebf7342daaa490b970568c1ea375e3242ebc4`  
		Last Modified: Tue, 19 Dec 2023 02:55:11 GMT  
		Size: 88.1 MB (88053431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a99edfe152899f2001989c0e6103ad6f2276cf961df3dbb4aceefec5312d373`  
		Last Modified: Tue, 19 Dec 2023 02:55:02 GMT  
		Size: 17.2 MB (17230056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20252565f8094ddee6562ad5f30ebc81e720ba92b526c0174372c3fad25e8625`  
		Last Modified: Tue, 19 Dec 2023 02:55:01 GMT  
		Size: 12.4 MB (12373194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df373a3b6f590305ac40bf712eb84f342145370ea6225181d41b1fe3229f6178`  
		Last Modified: Tue, 19 Dec 2023 02:55:44 GMT  
		Size: 303.9 MB (303857504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0`

```console
$ docker pull haskell@sha256:837f36cafcb26b3bf490c3032c2fc5e9a958310e084e90c5e64285887ccf4cfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.0` - linux; amd64

```console
$ docker pull haskell@sha256:c015b46959c871b5ef40e3dbf9126d4b0dab6caa01f39db4df1356ec615dba98
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **717.1 MB (717133390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1780cc5e360bf1bbaac2a2f6023b02e1f0ae99be7e196f42d0020a7803070db1`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:08 GMT
ADD file:4f8b7a35280160ec5a55323fa07ac91e294c86e2ea647ba212053983ef380bcf in / 
# Tue, 21 Nov 2023 05:22:08 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:55:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:56:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:57:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:47 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:39:51 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:39:55 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:39:58 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:54:27 GMT
ARG LLVM_VERSION=12
# Tue, 21 Nov 2023 12:54:27 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 21 Nov 2023 12:54:28 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 21 Nov 2023 12:54:28 GMT
ARG GHC=9.0.2
# Tue, 21 Nov 2023 12:54:28 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 21 Nov 2023 12:55:37 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:55:44 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:55:44 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b32028968d56a86ac35eac062e7abba276c547ab175fb057973c469eb41db55b`  
		Last Modified: Tue, 21 Nov 2023 05:26:57 GMT  
		Size: 50.5 MB (50499471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24c059838ae87ccefc35d50177e4e280a9e6f2f54127456ad0eaa5be5ed5386`  
		Last Modified: Tue, 21 Nov 2023 10:03:28 GMT  
		Size: 17.6 MB (17583860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819458a39dea8d30616a22068e79bcb7743745aa8b0d35fdb762ba69d98e3ec0`  
		Last Modified: Tue, 21 Nov 2023 10:03:45 GMT  
		Size: 51.9 MB (51874180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedd23d9034d9de62653c3bb2a2ca71fb88a1c6d17f386c0bfe4ac5bf8163929`  
		Last Modified: Tue, 21 Nov 2023 10:04:21 GMT  
		Size: 191.9 MB (191910019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ef9a56930d28877c2fa90904a7be44f1f8cca3356383b7f74682c75d8d994`  
		Last Modified: Tue, 21 Nov 2023 12:57:42 GMT  
		Size: 515.2 KB (515154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a1f56bfe415e8ae3055b472ce7df60a5bdf1033339c4dd235e31d400eb34c3`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 15.4 MB (15359949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35eecb76c7d0d3257ad0d1322fa0f70fe5bb08f73cd35791e40dedfeb7df855e`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d471e7e1cc00d7455cbcb5e330c0460e42a8e779f449883ae0a406e249dd35cc`  
		Last Modified: Tue, 21 Nov 2023 13:09:18 GMT  
		Size: 381.6 MB (381552389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.0` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:b9bfa4e6bc9825c695b7073dec09df2d61ab3249d4c8b0c367087ac63ed50dc1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.8 MB (641758454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:455eb16e8c3ffe22c38defa18a9706d07504a0160c0a7579c48a65007addcfb8`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:27 GMT
ADD file:ea38b381ee92d0c4b34697af5b78def83b881e6837b309e1f41a14bee2ff2b7e in / 
# Tue, 21 Nov 2023 06:27:27 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:00:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:00:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:01:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:18 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 08:21:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 08:21:25 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 08:21:28 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 08:36:21 GMT
ARG LLVM_VERSION=12
# Tue, 21 Nov 2023 08:36:21 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 21 Nov 2023 08:36:30 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 21 Nov 2023 08:36:30 GMT
ARG GHC=9.0.2
# Tue, 21 Nov 2023 08:36:30 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 21 Nov 2023 08:37:13 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 08:37:23 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 08:37:23 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:357c576c57e480da5e7eb018506db51d822da9f357c02a76f7c4da1ccaa61b33`  
		Last Modified: Tue, 21 Nov 2023 06:31:24 GMT  
		Size: 49.3 MB (49291145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9750a1d4e9cc8d118fb8f247658f2e931026ab641d4ebdc3c3806b3dd8ee4d0d`  
		Last Modified: Tue, 21 Nov 2023 08:07:51 GMT  
		Size: 17.5 MB (17454097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55295586deeb07a4153f5f4d0cd2723a2240e52697d6ad85612c498057c0d832`  
		Last Modified: Tue, 21 Nov 2023 08:08:06 GMT  
		Size: 52.2 MB (52207152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fb9e461a1bbc28daea6d98c6425175d5ec238091b9c6d22306c3d257de50cd`  
		Last Modified: Tue, 21 Nov 2023 08:08:31 GMT  
		Size: 183.5 MB (183476090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8520593e4d4d8289c877a174b696c2830f14eb2b1b3a3a832ad50cb64aa23049`  
		Last Modified: Tue, 21 Nov 2023 08:39:07 GMT  
		Size: 517.3 KB (517300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234bbe5f5278dc328477465898a776d8addb6172cfc0ae55d199f015a74987c`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 17.2 MB (17230042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ed20186e4d0efa5eec675e66c421203c5fe383a529511ab58816cb659b96a0`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 12.4 MB (12373189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c619f83ed516b75c23ae61b39bb6ef0ea3845490960453d2e96112c3e05e85e`  
		Last Modified: Tue, 21 Nov 2023 08:49:04 GMT  
		Size: 45.9 MB (45889738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3a7d7d3b67d905a0d1632124cb4ab9287268cf8b9e67632de7162cfe1a35a6`  
		Last Modified: Tue, 21 Nov 2023 08:49:44 GMT  
		Size: 263.3 MB (263319701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0-buster`

```console
$ docker pull haskell@sha256:837f36cafcb26b3bf490c3032c2fc5e9a958310e084e90c5e64285887ccf4cfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.0-buster` - linux; amd64

```console
$ docker pull haskell@sha256:c015b46959c871b5ef40e3dbf9126d4b0dab6caa01f39db4df1356ec615dba98
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **717.1 MB (717133390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1780cc5e360bf1bbaac2a2f6023b02e1f0ae99be7e196f42d0020a7803070db1`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:08 GMT
ADD file:4f8b7a35280160ec5a55323fa07ac91e294c86e2ea647ba212053983ef380bcf in / 
# Tue, 21 Nov 2023 05:22:08 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:55:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:56:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:57:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:47 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:39:51 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:39:55 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:39:58 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:54:27 GMT
ARG LLVM_VERSION=12
# Tue, 21 Nov 2023 12:54:27 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 21 Nov 2023 12:54:28 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 21 Nov 2023 12:54:28 GMT
ARG GHC=9.0.2
# Tue, 21 Nov 2023 12:54:28 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 21 Nov 2023 12:55:37 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:55:44 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:55:44 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b32028968d56a86ac35eac062e7abba276c547ab175fb057973c469eb41db55b`  
		Last Modified: Tue, 21 Nov 2023 05:26:57 GMT  
		Size: 50.5 MB (50499471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24c059838ae87ccefc35d50177e4e280a9e6f2f54127456ad0eaa5be5ed5386`  
		Last Modified: Tue, 21 Nov 2023 10:03:28 GMT  
		Size: 17.6 MB (17583860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819458a39dea8d30616a22068e79bcb7743745aa8b0d35fdb762ba69d98e3ec0`  
		Last Modified: Tue, 21 Nov 2023 10:03:45 GMT  
		Size: 51.9 MB (51874180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedd23d9034d9de62653c3bb2a2ca71fb88a1c6d17f386c0bfe4ac5bf8163929`  
		Last Modified: Tue, 21 Nov 2023 10:04:21 GMT  
		Size: 191.9 MB (191910019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ef9a56930d28877c2fa90904a7be44f1f8cca3356383b7f74682c75d8d994`  
		Last Modified: Tue, 21 Nov 2023 12:57:42 GMT  
		Size: 515.2 KB (515154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a1f56bfe415e8ae3055b472ce7df60a5bdf1033339c4dd235e31d400eb34c3`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 15.4 MB (15359949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35eecb76c7d0d3257ad0d1322fa0f70fe5bb08f73cd35791e40dedfeb7df855e`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d471e7e1cc00d7455cbcb5e330c0460e42a8e779f449883ae0a406e249dd35cc`  
		Last Modified: Tue, 21 Nov 2023 13:09:18 GMT  
		Size: 381.6 MB (381552389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.0-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:b9bfa4e6bc9825c695b7073dec09df2d61ab3249d4c8b0c367087ac63ed50dc1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.8 MB (641758454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:455eb16e8c3ffe22c38defa18a9706d07504a0160c0a7579c48a65007addcfb8`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:27 GMT
ADD file:ea38b381ee92d0c4b34697af5b78def83b881e6837b309e1f41a14bee2ff2b7e in / 
# Tue, 21 Nov 2023 06:27:27 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:00:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:00:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:01:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:18 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 08:21:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 08:21:25 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 08:21:28 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 08:36:21 GMT
ARG LLVM_VERSION=12
# Tue, 21 Nov 2023 08:36:21 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 21 Nov 2023 08:36:30 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 21 Nov 2023 08:36:30 GMT
ARG GHC=9.0.2
# Tue, 21 Nov 2023 08:36:30 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 21 Nov 2023 08:37:13 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 08:37:23 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 08:37:23 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:357c576c57e480da5e7eb018506db51d822da9f357c02a76f7c4da1ccaa61b33`  
		Last Modified: Tue, 21 Nov 2023 06:31:24 GMT  
		Size: 49.3 MB (49291145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9750a1d4e9cc8d118fb8f247658f2e931026ab641d4ebdc3c3806b3dd8ee4d0d`  
		Last Modified: Tue, 21 Nov 2023 08:07:51 GMT  
		Size: 17.5 MB (17454097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55295586deeb07a4153f5f4d0cd2723a2240e52697d6ad85612c498057c0d832`  
		Last Modified: Tue, 21 Nov 2023 08:08:06 GMT  
		Size: 52.2 MB (52207152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fb9e461a1bbc28daea6d98c6425175d5ec238091b9c6d22306c3d257de50cd`  
		Last Modified: Tue, 21 Nov 2023 08:08:31 GMT  
		Size: 183.5 MB (183476090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8520593e4d4d8289c877a174b696c2830f14eb2b1b3a3a832ad50cb64aa23049`  
		Last Modified: Tue, 21 Nov 2023 08:39:07 GMT  
		Size: 517.3 KB (517300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234bbe5f5278dc328477465898a776d8addb6172cfc0ae55d199f015a74987c`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 17.2 MB (17230042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ed20186e4d0efa5eec675e66c421203c5fe383a529511ab58816cb659b96a0`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 12.4 MB (12373189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c619f83ed516b75c23ae61b39bb6ef0ea3845490960453d2e96112c3e05e85e`  
		Last Modified: Tue, 21 Nov 2023 08:49:04 GMT  
		Size: 45.9 MB (45889738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3a7d7d3b67d905a0d1632124cb4ab9287268cf8b9e67632de7162cfe1a35a6`  
		Last Modified: Tue, 21 Nov 2023 08:49:44 GMT  
		Size: 263.3 MB (263319701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0-slim`

```console
$ docker pull haskell@sha256:4b983daec4d6d18b03e2de0a7ef52a4e9d5cb739cf937d8ec27e4dda4034805f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.0-slim` - linux; amd64

```console
$ docker pull haskell@sha256:fffa571e609ab5b53c0810427a80416055b629fb4793dd718739148299598edb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **409.6 MB (409553491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68db3b9ddb322124dee6635a209686255533da0f759963d20797037d45544823`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:20 GMT
ADD file:7672eb709be933bb0edec47b8141cd2ebff266a770dfae1278205f7cee43c71a in / 
# Tue, 21 Nov 2023 05:22:20 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:41:56 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:42:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:42:21 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:42:24 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:55:51 GMT
ARG LLVM_VERSION=12
# Tue, 21 Nov 2023 12:55:51 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 21 Nov 2023 12:55:51 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 21 Nov 2023 12:55:51 GMT
ARG GHC=9.0.2
# Tue, 21 Nov 2023 12:55:51 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 21 Nov 2023 12:56:58 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:57:04 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:57:04 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0fc9206bc4affb32fe13185a20b8184271c753e9b7cb81484bf770054fc69737`  
		Last Modified: Tue, 21 Nov 2023 05:27:19 GMT  
		Size: 27.2 MB (27187457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6213b4299e71dcc2c16c339ec043da12cc47384caa53a9f15259996652e6bf4`  
		Last Modified: Tue, 21 Nov 2023 12:59:36 GMT  
		Size: 94.0 MB (94045021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19344eacbd857e0b61cb66092db6d11c467aed149978f45a1dcdb057ebb9980`  
		Last Modified: Tue, 21 Nov 2023 12:59:24 GMT  
		Size: 15.4 MB (15359960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefb56630c3948901bac3dd75868f7d017f4b46579498b8fdf054347f3db9894`  
		Last Modified: Tue, 21 Nov 2023 12:59:23 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33f8318aab0fa0cad999c6c3e77c68158738ef79c5393e2d80886dcc0a2ce91`  
		Last Modified: Tue, 21 Nov 2023 13:10:21 GMT  
		Size: 265.1 MB (265122685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.0-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:70115f460f79fa1d29acc4e82aff9e12168b48fe1c45f66af1362f015c5256b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.8 MB (466777029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ed3a530a0f915b5e3e44b882c8aabd8ad7949dafec8f9badba0dce9bd29d7d`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:39 GMT
ADD file:f60673c303a98b4e4c676e3403bc1b7cb316335aba1202205188176810494c07 in / 
# Tue, 19 Dec 2023 01:41:40 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:46:03 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 02:46:21 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK=2.11.1
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 19 Dec 2023 02:46:31 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 19 Dec 2023 02:46:34 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 19 Dec 2023 02:53:26 GMT
ARG LLVM_VERSION=12
# Tue, 19 Dec 2023 02:53:26 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 19 Dec 2023 02:53:34 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 19 Dec 2023 02:53:35 GMT
ARG GHC=9.0.2
# Tue, 19 Dec 2023 02:53:35 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 19 Dec 2023 02:54:17 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 19 Dec 2023 02:54:26 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 02:54:26 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c0b0171eefd1c6d7f85c54d4a609269c9b5e19a0fd8cd787a49c808c6b73cf74`  
		Last Modified: Tue, 19 Dec 2023 01:46:01 GMT  
		Size: 26.0 MB (25969827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6ed82599775f9bbd4cc3c5df2ebf7342daaa490b970568c1ea375e3242ebc4`  
		Last Modified: Tue, 19 Dec 2023 02:55:11 GMT  
		Size: 88.1 MB (88053431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a99edfe152899f2001989c0e6103ad6f2276cf961df3dbb4aceefec5312d373`  
		Last Modified: Tue, 19 Dec 2023 02:55:02 GMT  
		Size: 17.2 MB (17230056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20252565f8094ddee6562ad5f30ebc81e720ba92b526c0174372c3fad25e8625`  
		Last Modified: Tue, 19 Dec 2023 02:55:01 GMT  
		Size: 12.4 MB (12373194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fac61a0760b78aab7262fb1597704b6d5de80c4636622f2e1e5c670854f77c0`  
		Last Modified: Tue, 19 Dec 2023 02:59:14 GMT  
		Size: 59.8 MB (59835982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51291ccbdae8083b3557bb530286c9dbece837cea1e787fcc3adfff4d8d88e30`  
		Last Modified: Tue, 19 Dec 2023 02:59:53 GMT  
		Size: 263.3 MB (263314539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0-slim-buster`

```console
$ docker pull haskell@sha256:4b983daec4d6d18b03e2de0a7ef52a4e9d5cb739cf937d8ec27e4dda4034805f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.0-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:fffa571e609ab5b53c0810427a80416055b629fb4793dd718739148299598edb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **409.6 MB (409553491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68db3b9ddb322124dee6635a209686255533da0f759963d20797037d45544823`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:20 GMT
ADD file:7672eb709be933bb0edec47b8141cd2ebff266a770dfae1278205f7cee43c71a in / 
# Tue, 21 Nov 2023 05:22:20 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:41:56 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:42:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:42:21 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:42:24 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:55:51 GMT
ARG LLVM_VERSION=12
# Tue, 21 Nov 2023 12:55:51 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 21 Nov 2023 12:55:51 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 21 Nov 2023 12:55:51 GMT
ARG GHC=9.0.2
# Tue, 21 Nov 2023 12:55:51 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 21 Nov 2023 12:56:58 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:57:04 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:57:04 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0fc9206bc4affb32fe13185a20b8184271c753e9b7cb81484bf770054fc69737`  
		Last Modified: Tue, 21 Nov 2023 05:27:19 GMT  
		Size: 27.2 MB (27187457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6213b4299e71dcc2c16c339ec043da12cc47384caa53a9f15259996652e6bf4`  
		Last Modified: Tue, 21 Nov 2023 12:59:36 GMT  
		Size: 94.0 MB (94045021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19344eacbd857e0b61cb66092db6d11c467aed149978f45a1dcdb057ebb9980`  
		Last Modified: Tue, 21 Nov 2023 12:59:24 GMT  
		Size: 15.4 MB (15359960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefb56630c3948901bac3dd75868f7d017f4b46579498b8fdf054347f3db9894`  
		Last Modified: Tue, 21 Nov 2023 12:59:23 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33f8318aab0fa0cad999c6c3e77c68158738ef79c5393e2d80886dcc0a2ce91`  
		Last Modified: Tue, 21 Nov 2023 13:10:21 GMT  
		Size: 265.1 MB (265122685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.0-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:70115f460f79fa1d29acc4e82aff9e12168b48fe1c45f66af1362f015c5256b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.8 MB (466777029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ed3a530a0f915b5e3e44b882c8aabd8ad7949dafec8f9badba0dce9bd29d7d`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:39 GMT
ADD file:f60673c303a98b4e4c676e3403bc1b7cb316335aba1202205188176810494c07 in / 
# Tue, 19 Dec 2023 01:41:40 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:46:03 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 02:46:21 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK=2.11.1
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 19 Dec 2023 02:46:31 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 19 Dec 2023 02:46:34 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 19 Dec 2023 02:53:26 GMT
ARG LLVM_VERSION=12
# Tue, 19 Dec 2023 02:53:26 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 19 Dec 2023 02:53:34 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 19 Dec 2023 02:53:35 GMT
ARG GHC=9.0.2
# Tue, 19 Dec 2023 02:53:35 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 19 Dec 2023 02:54:17 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 19 Dec 2023 02:54:26 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 02:54:26 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c0b0171eefd1c6d7f85c54d4a609269c9b5e19a0fd8cd787a49c808c6b73cf74`  
		Last Modified: Tue, 19 Dec 2023 01:46:01 GMT  
		Size: 26.0 MB (25969827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6ed82599775f9bbd4cc3c5df2ebf7342daaa490b970568c1ea375e3242ebc4`  
		Last Modified: Tue, 19 Dec 2023 02:55:11 GMT  
		Size: 88.1 MB (88053431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a99edfe152899f2001989c0e6103ad6f2276cf961df3dbb4aceefec5312d373`  
		Last Modified: Tue, 19 Dec 2023 02:55:02 GMT  
		Size: 17.2 MB (17230056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20252565f8094ddee6562ad5f30ebc81e720ba92b526c0174372c3fad25e8625`  
		Last Modified: Tue, 19 Dec 2023 02:55:01 GMT  
		Size: 12.4 MB (12373194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fac61a0760b78aab7262fb1597704b6d5de80c4636622f2e1e5c670854f77c0`  
		Last Modified: Tue, 19 Dec 2023 02:59:14 GMT  
		Size: 59.8 MB (59835982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51291ccbdae8083b3557bb530286c9dbece837cea1e787fcc3adfff4d8d88e30`  
		Last Modified: Tue, 19 Dec 2023 02:59:53 GMT  
		Size: 263.3 MB (263314539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0.2`

```console
$ docker pull haskell@sha256:837f36cafcb26b3bf490c3032c2fc5e9a958310e084e90c5e64285887ccf4cfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.0.2` - linux; amd64

```console
$ docker pull haskell@sha256:c015b46959c871b5ef40e3dbf9126d4b0dab6caa01f39db4df1356ec615dba98
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **717.1 MB (717133390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1780cc5e360bf1bbaac2a2f6023b02e1f0ae99be7e196f42d0020a7803070db1`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:08 GMT
ADD file:4f8b7a35280160ec5a55323fa07ac91e294c86e2ea647ba212053983ef380bcf in / 
# Tue, 21 Nov 2023 05:22:08 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:55:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:56:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:57:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:47 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:39:51 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:39:55 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:39:58 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:54:27 GMT
ARG LLVM_VERSION=12
# Tue, 21 Nov 2023 12:54:27 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 21 Nov 2023 12:54:28 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 21 Nov 2023 12:54:28 GMT
ARG GHC=9.0.2
# Tue, 21 Nov 2023 12:54:28 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 21 Nov 2023 12:55:37 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:55:44 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:55:44 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b32028968d56a86ac35eac062e7abba276c547ab175fb057973c469eb41db55b`  
		Last Modified: Tue, 21 Nov 2023 05:26:57 GMT  
		Size: 50.5 MB (50499471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24c059838ae87ccefc35d50177e4e280a9e6f2f54127456ad0eaa5be5ed5386`  
		Last Modified: Tue, 21 Nov 2023 10:03:28 GMT  
		Size: 17.6 MB (17583860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819458a39dea8d30616a22068e79bcb7743745aa8b0d35fdb762ba69d98e3ec0`  
		Last Modified: Tue, 21 Nov 2023 10:03:45 GMT  
		Size: 51.9 MB (51874180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedd23d9034d9de62653c3bb2a2ca71fb88a1c6d17f386c0bfe4ac5bf8163929`  
		Last Modified: Tue, 21 Nov 2023 10:04:21 GMT  
		Size: 191.9 MB (191910019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ef9a56930d28877c2fa90904a7be44f1f8cca3356383b7f74682c75d8d994`  
		Last Modified: Tue, 21 Nov 2023 12:57:42 GMT  
		Size: 515.2 KB (515154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a1f56bfe415e8ae3055b472ce7df60a5bdf1033339c4dd235e31d400eb34c3`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 15.4 MB (15359949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35eecb76c7d0d3257ad0d1322fa0f70fe5bb08f73cd35791e40dedfeb7df855e`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d471e7e1cc00d7455cbcb5e330c0460e42a8e779f449883ae0a406e249dd35cc`  
		Last Modified: Tue, 21 Nov 2023 13:09:18 GMT  
		Size: 381.6 MB (381552389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.0.2` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:b9bfa4e6bc9825c695b7073dec09df2d61ab3249d4c8b0c367087ac63ed50dc1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.8 MB (641758454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:455eb16e8c3ffe22c38defa18a9706d07504a0160c0a7579c48a65007addcfb8`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:27 GMT
ADD file:ea38b381ee92d0c4b34697af5b78def83b881e6837b309e1f41a14bee2ff2b7e in / 
# Tue, 21 Nov 2023 06:27:27 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:00:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:00:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:01:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:18 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 08:21:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 08:21:25 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 08:21:28 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 08:36:21 GMT
ARG LLVM_VERSION=12
# Tue, 21 Nov 2023 08:36:21 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 21 Nov 2023 08:36:30 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 21 Nov 2023 08:36:30 GMT
ARG GHC=9.0.2
# Tue, 21 Nov 2023 08:36:30 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 21 Nov 2023 08:37:13 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 08:37:23 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 08:37:23 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:357c576c57e480da5e7eb018506db51d822da9f357c02a76f7c4da1ccaa61b33`  
		Last Modified: Tue, 21 Nov 2023 06:31:24 GMT  
		Size: 49.3 MB (49291145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9750a1d4e9cc8d118fb8f247658f2e931026ab641d4ebdc3c3806b3dd8ee4d0d`  
		Last Modified: Tue, 21 Nov 2023 08:07:51 GMT  
		Size: 17.5 MB (17454097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55295586deeb07a4153f5f4d0cd2723a2240e52697d6ad85612c498057c0d832`  
		Last Modified: Tue, 21 Nov 2023 08:08:06 GMT  
		Size: 52.2 MB (52207152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fb9e461a1bbc28daea6d98c6425175d5ec238091b9c6d22306c3d257de50cd`  
		Last Modified: Tue, 21 Nov 2023 08:08:31 GMT  
		Size: 183.5 MB (183476090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8520593e4d4d8289c877a174b696c2830f14eb2b1b3a3a832ad50cb64aa23049`  
		Last Modified: Tue, 21 Nov 2023 08:39:07 GMT  
		Size: 517.3 KB (517300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234bbe5f5278dc328477465898a776d8addb6172cfc0ae55d199f015a74987c`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 17.2 MB (17230042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ed20186e4d0efa5eec675e66c421203c5fe383a529511ab58816cb659b96a0`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 12.4 MB (12373189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c619f83ed516b75c23ae61b39bb6ef0ea3845490960453d2e96112c3e05e85e`  
		Last Modified: Tue, 21 Nov 2023 08:49:04 GMT  
		Size: 45.9 MB (45889738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3a7d7d3b67d905a0d1632124cb4ab9287268cf8b9e67632de7162cfe1a35a6`  
		Last Modified: Tue, 21 Nov 2023 08:49:44 GMT  
		Size: 263.3 MB (263319701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0.2-buster`

```console
$ docker pull haskell@sha256:837f36cafcb26b3bf490c3032c2fc5e9a958310e084e90c5e64285887ccf4cfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.0.2-buster` - linux; amd64

```console
$ docker pull haskell@sha256:c015b46959c871b5ef40e3dbf9126d4b0dab6caa01f39db4df1356ec615dba98
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **717.1 MB (717133390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1780cc5e360bf1bbaac2a2f6023b02e1f0ae99be7e196f42d0020a7803070db1`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:08 GMT
ADD file:4f8b7a35280160ec5a55323fa07ac91e294c86e2ea647ba212053983ef380bcf in / 
# Tue, 21 Nov 2023 05:22:08 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:55:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:56:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:57:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:47 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:39:51 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:39:55 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:39:58 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:54:27 GMT
ARG LLVM_VERSION=12
# Tue, 21 Nov 2023 12:54:27 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 21 Nov 2023 12:54:28 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 21 Nov 2023 12:54:28 GMT
ARG GHC=9.0.2
# Tue, 21 Nov 2023 12:54:28 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 21 Nov 2023 12:55:37 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:55:44 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:55:44 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b32028968d56a86ac35eac062e7abba276c547ab175fb057973c469eb41db55b`  
		Last Modified: Tue, 21 Nov 2023 05:26:57 GMT  
		Size: 50.5 MB (50499471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24c059838ae87ccefc35d50177e4e280a9e6f2f54127456ad0eaa5be5ed5386`  
		Last Modified: Tue, 21 Nov 2023 10:03:28 GMT  
		Size: 17.6 MB (17583860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819458a39dea8d30616a22068e79bcb7743745aa8b0d35fdb762ba69d98e3ec0`  
		Last Modified: Tue, 21 Nov 2023 10:03:45 GMT  
		Size: 51.9 MB (51874180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedd23d9034d9de62653c3bb2a2ca71fb88a1c6d17f386c0bfe4ac5bf8163929`  
		Last Modified: Tue, 21 Nov 2023 10:04:21 GMT  
		Size: 191.9 MB (191910019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ef9a56930d28877c2fa90904a7be44f1f8cca3356383b7f74682c75d8d994`  
		Last Modified: Tue, 21 Nov 2023 12:57:42 GMT  
		Size: 515.2 KB (515154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a1f56bfe415e8ae3055b472ce7df60a5bdf1033339c4dd235e31d400eb34c3`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 15.4 MB (15359949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35eecb76c7d0d3257ad0d1322fa0f70fe5bb08f73cd35791e40dedfeb7df855e`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d471e7e1cc00d7455cbcb5e330c0460e42a8e779f449883ae0a406e249dd35cc`  
		Last Modified: Tue, 21 Nov 2023 13:09:18 GMT  
		Size: 381.6 MB (381552389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.0.2-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:b9bfa4e6bc9825c695b7073dec09df2d61ab3249d4c8b0c367087ac63ed50dc1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.8 MB (641758454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:455eb16e8c3ffe22c38defa18a9706d07504a0160c0a7579c48a65007addcfb8`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:27 GMT
ADD file:ea38b381ee92d0c4b34697af5b78def83b881e6837b309e1f41a14bee2ff2b7e in / 
# Tue, 21 Nov 2023 06:27:27 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:00:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:00:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:01:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:18 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 08:21:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 08:21:25 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 08:21:28 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 08:36:21 GMT
ARG LLVM_VERSION=12
# Tue, 21 Nov 2023 08:36:21 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 21 Nov 2023 08:36:30 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 21 Nov 2023 08:36:30 GMT
ARG GHC=9.0.2
# Tue, 21 Nov 2023 08:36:30 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 21 Nov 2023 08:37:13 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 08:37:23 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 08:37:23 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:357c576c57e480da5e7eb018506db51d822da9f357c02a76f7c4da1ccaa61b33`  
		Last Modified: Tue, 21 Nov 2023 06:31:24 GMT  
		Size: 49.3 MB (49291145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9750a1d4e9cc8d118fb8f247658f2e931026ab641d4ebdc3c3806b3dd8ee4d0d`  
		Last Modified: Tue, 21 Nov 2023 08:07:51 GMT  
		Size: 17.5 MB (17454097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55295586deeb07a4153f5f4d0cd2723a2240e52697d6ad85612c498057c0d832`  
		Last Modified: Tue, 21 Nov 2023 08:08:06 GMT  
		Size: 52.2 MB (52207152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fb9e461a1bbc28daea6d98c6425175d5ec238091b9c6d22306c3d257de50cd`  
		Last Modified: Tue, 21 Nov 2023 08:08:31 GMT  
		Size: 183.5 MB (183476090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8520593e4d4d8289c877a174b696c2830f14eb2b1b3a3a832ad50cb64aa23049`  
		Last Modified: Tue, 21 Nov 2023 08:39:07 GMT  
		Size: 517.3 KB (517300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234bbe5f5278dc328477465898a776d8addb6172cfc0ae55d199f015a74987c`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 17.2 MB (17230042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ed20186e4d0efa5eec675e66c421203c5fe383a529511ab58816cb659b96a0`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 12.4 MB (12373189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c619f83ed516b75c23ae61b39bb6ef0ea3845490960453d2e96112c3e05e85e`  
		Last Modified: Tue, 21 Nov 2023 08:49:04 GMT  
		Size: 45.9 MB (45889738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b3a7d7d3b67d905a0d1632124cb4ab9287268cf8b9e67632de7162cfe1a35a6`  
		Last Modified: Tue, 21 Nov 2023 08:49:44 GMT  
		Size: 263.3 MB (263319701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0.2-slim`

```console
$ docker pull haskell@sha256:4b983daec4d6d18b03e2de0a7ef52a4e9d5cb739cf937d8ec27e4dda4034805f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.0.2-slim` - linux; amd64

```console
$ docker pull haskell@sha256:fffa571e609ab5b53c0810427a80416055b629fb4793dd718739148299598edb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **409.6 MB (409553491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68db3b9ddb322124dee6635a209686255533da0f759963d20797037d45544823`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:20 GMT
ADD file:7672eb709be933bb0edec47b8141cd2ebff266a770dfae1278205f7cee43c71a in / 
# Tue, 21 Nov 2023 05:22:20 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:41:56 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:42:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:42:21 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:42:24 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:55:51 GMT
ARG LLVM_VERSION=12
# Tue, 21 Nov 2023 12:55:51 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 21 Nov 2023 12:55:51 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 21 Nov 2023 12:55:51 GMT
ARG GHC=9.0.2
# Tue, 21 Nov 2023 12:55:51 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 21 Nov 2023 12:56:58 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:57:04 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:57:04 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0fc9206bc4affb32fe13185a20b8184271c753e9b7cb81484bf770054fc69737`  
		Last Modified: Tue, 21 Nov 2023 05:27:19 GMT  
		Size: 27.2 MB (27187457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6213b4299e71dcc2c16c339ec043da12cc47384caa53a9f15259996652e6bf4`  
		Last Modified: Tue, 21 Nov 2023 12:59:36 GMT  
		Size: 94.0 MB (94045021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19344eacbd857e0b61cb66092db6d11c467aed149978f45a1dcdb057ebb9980`  
		Last Modified: Tue, 21 Nov 2023 12:59:24 GMT  
		Size: 15.4 MB (15359960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefb56630c3948901bac3dd75868f7d017f4b46579498b8fdf054347f3db9894`  
		Last Modified: Tue, 21 Nov 2023 12:59:23 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33f8318aab0fa0cad999c6c3e77c68158738ef79c5393e2d80886dcc0a2ce91`  
		Last Modified: Tue, 21 Nov 2023 13:10:21 GMT  
		Size: 265.1 MB (265122685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.0.2-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:70115f460f79fa1d29acc4e82aff9e12168b48fe1c45f66af1362f015c5256b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.8 MB (466777029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ed3a530a0f915b5e3e44b882c8aabd8ad7949dafec8f9badba0dce9bd29d7d`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:39 GMT
ADD file:f60673c303a98b4e4c676e3403bc1b7cb316335aba1202205188176810494c07 in / 
# Tue, 19 Dec 2023 01:41:40 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:46:03 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 02:46:21 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK=2.11.1
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 19 Dec 2023 02:46:31 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 19 Dec 2023 02:46:34 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 19 Dec 2023 02:53:26 GMT
ARG LLVM_VERSION=12
# Tue, 19 Dec 2023 02:53:26 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 19 Dec 2023 02:53:34 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 19 Dec 2023 02:53:35 GMT
ARG GHC=9.0.2
# Tue, 19 Dec 2023 02:53:35 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 19 Dec 2023 02:54:17 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 19 Dec 2023 02:54:26 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 02:54:26 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c0b0171eefd1c6d7f85c54d4a609269c9b5e19a0fd8cd787a49c808c6b73cf74`  
		Last Modified: Tue, 19 Dec 2023 01:46:01 GMT  
		Size: 26.0 MB (25969827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6ed82599775f9bbd4cc3c5df2ebf7342daaa490b970568c1ea375e3242ebc4`  
		Last Modified: Tue, 19 Dec 2023 02:55:11 GMT  
		Size: 88.1 MB (88053431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a99edfe152899f2001989c0e6103ad6f2276cf961df3dbb4aceefec5312d373`  
		Last Modified: Tue, 19 Dec 2023 02:55:02 GMT  
		Size: 17.2 MB (17230056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20252565f8094ddee6562ad5f30ebc81e720ba92b526c0174372c3fad25e8625`  
		Last Modified: Tue, 19 Dec 2023 02:55:01 GMT  
		Size: 12.4 MB (12373194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fac61a0760b78aab7262fb1597704b6d5de80c4636622f2e1e5c670854f77c0`  
		Last Modified: Tue, 19 Dec 2023 02:59:14 GMT  
		Size: 59.8 MB (59835982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51291ccbdae8083b3557bb530286c9dbece837cea1e787fcc3adfff4d8d88e30`  
		Last Modified: Tue, 19 Dec 2023 02:59:53 GMT  
		Size: 263.3 MB (263314539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0.2-slim-buster`

```console
$ docker pull haskell@sha256:4b983daec4d6d18b03e2de0a7ef52a4e9d5cb739cf937d8ec27e4dda4034805f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.0.2-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:fffa571e609ab5b53c0810427a80416055b629fb4793dd718739148299598edb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **409.6 MB (409553491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68db3b9ddb322124dee6635a209686255533da0f759963d20797037d45544823`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:20 GMT
ADD file:7672eb709be933bb0edec47b8141cd2ebff266a770dfae1278205f7cee43c71a in / 
# Tue, 21 Nov 2023 05:22:20 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:41:56 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:42:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:42:21 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:42:24 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:55:51 GMT
ARG LLVM_VERSION=12
# Tue, 21 Nov 2023 12:55:51 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 21 Nov 2023 12:55:51 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 21 Nov 2023 12:55:51 GMT
ARG GHC=9.0.2
# Tue, 21 Nov 2023 12:55:51 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 21 Nov 2023 12:56:58 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:57:04 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:57:04 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0fc9206bc4affb32fe13185a20b8184271c753e9b7cb81484bf770054fc69737`  
		Last Modified: Tue, 21 Nov 2023 05:27:19 GMT  
		Size: 27.2 MB (27187457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6213b4299e71dcc2c16c339ec043da12cc47384caa53a9f15259996652e6bf4`  
		Last Modified: Tue, 21 Nov 2023 12:59:36 GMT  
		Size: 94.0 MB (94045021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19344eacbd857e0b61cb66092db6d11c467aed149978f45a1dcdb057ebb9980`  
		Last Modified: Tue, 21 Nov 2023 12:59:24 GMT  
		Size: 15.4 MB (15359960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefb56630c3948901bac3dd75868f7d017f4b46579498b8fdf054347f3db9894`  
		Last Modified: Tue, 21 Nov 2023 12:59:23 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33f8318aab0fa0cad999c6c3e77c68158738ef79c5393e2d80886dcc0a2ce91`  
		Last Modified: Tue, 21 Nov 2023 13:10:21 GMT  
		Size: 265.1 MB (265122685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.0.2-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:70115f460f79fa1d29acc4e82aff9e12168b48fe1c45f66af1362f015c5256b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.8 MB (466777029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ed3a530a0f915b5e3e44b882c8aabd8ad7949dafec8f9badba0dce9bd29d7d`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:39 GMT
ADD file:f60673c303a98b4e4c676e3403bc1b7cb316335aba1202205188176810494c07 in / 
# Tue, 19 Dec 2023 01:41:40 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:46:03 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 02:46:21 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK=2.11.1
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 19 Dec 2023 02:46:31 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 19 Dec 2023 02:46:34 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 19 Dec 2023 02:53:26 GMT
ARG LLVM_VERSION=12
# Tue, 19 Dec 2023 02:53:26 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 19 Dec 2023 02:53:34 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 19 Dec 2023 02:53:35 GMT
ARG GHC=9.0.2
# Tue, 19 Dec 2023 02:53:35 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 19 Dec 2023 02:54:17 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 19 Dec 2023 02:54:26 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 02:54:26 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c0b0171eefd1c6d7f85c54d4a609269c9b5e19a0fd8cd787a49c808c6b73cf74`  
		Last Modified: Tue, 19 Dec 2023 01:46:01 GMT  
		Size: 26.0 MB (25969827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6ed82599775f9bbd4cc3c5df2ebf7342daaa490b970568c1ea375e3242ebc4`  
		Last Modified: Tue, 19 Dec 2023 02:55:11 GMT  
		Size: 88.1 MB (88053431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a99edfe152899f2001989c0e6103ad6f2276cf961df3dbb4aceefec5312d373`  
		Last Modified: Tue, 19 Dec 2023 02:55:02 GMT  
		Size: 17.2 MB (17230056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20252565f8094ddee6562ad5f30ebc81e720ba92b526c0174372c3fad25e8625`  
		Last Modified: Tue, 19 Dec 2023 02:55:01 GMT  
		Size: 12.4 MB (12373194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fac61a0760b78aab7262fb1597704b6d5de80c4636622f2e1e5c670854f77c0`  
		Last Modified: Tue, 19 Dec 2023 02:59:14 GMT  
		Size: 59.8 MB (59835982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51291ccbdae8083b3557bb530286c9dbece837cea1e787fcc3adfff4d8d88e30`  
		Last Modified: Tue, 19 Dec 2023 02:59:53 GMT  
		Size: 263.3 MB (263314539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.2`

```console
$ docker pull haskell@sha256:c4bd03e247cd0c39c700990bb42f6e347006e0ebcb8e1358b4ac4262b64ea26d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.2` - linux; amd64

```console
$ docker pull haskell@sha256:bad6b18e695d9e6e2f73443c60a3ad19c8d74273217a63bd744ad6d82ac53114
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **735.8 MB (735806049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:626f75b9d7f657f06c6201ba4e43ea28a791918b358363d483f062ac11c0354e`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:08 GMT
ADD file:4f8b7a35280160ec5a55323fa07ac91e294c86e2ea647ba212053983ef380bcf in / 
# Tue, 21 Nov 2023 05:22:08 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:55:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:56:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:57:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:47 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:39:51 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:39:55 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:39:58 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:51:39 GMT
ARG GHC=9.2.8
# Tue, 21 Nov 2023 12:51:40 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 21 Nov 2023 12:52:51 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.8 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='645433359d8ad9e7b286f85ef5111db1b787ee3712c24c5dfde7c62769aa59a4';             ;;         'x86_64')             GHC_SHA256='10d1be25487bcf99ac8eb77beaa220c85e69f8c1106f4219ce019206ecc0ac51';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:52:58 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:52:58 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b32028968d56a86ac35eac062e7abba276c547ab175fb057973c469eb41db55b`  
		Last Modified: Tue, 21 Nov 2023 05:26:57 GMT  
		Size: 50.5 MB (50499471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24c059838ae87ccefc35d50177e4e280a9e6f2f54127456ad0eaa5be5ed5386`  
		Last Modified: Tue, 21 Nov 2023 10:03:28 GMT  
		Size: 17.6 MB (17583860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819458a39dea8d30616a22068e79bcb7743745aa8b0d35fdb762ba69d98e3ec0`  
		Last Modified: Tue, 21 Nov 2023 10:03:45 GMT  
		Size: 51.9 MB (51874180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedd23d9034d9de62653c3bb2a2ca71fb88a1c6d17f386c0bfe4ac5bf8163929`  
		Last Modified: Tue, 21 Nov 2023 10:04:21 GMT  
		Size: 191.9 MB (191910019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ef9a56930d28877c2fa90904a7be44f1f8cca3356383b7f74682c75d8d994`  
		Last Modified: Tue, 21 Nov 2023 12:57:42 GMT  
		Size: 515.2 KB (515154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a1f56bfe415e8ae3055b472ce7df60a5bdf1033339c4dd235e31d400eb34c3`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 15.4 MB (15359949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35eecb76c7d0d3257ad0d1322fa0f70fe5bb08f73cd35791e40dedfeb7df855e`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f0eeefb5db658b0a0a28b275aba9c98ec4c18cfc690c89bea3da6890017a35`  
		Last Modified: Tue, 21 Nov 2023 13:06:47 GMT  
		Size: 400.2 MB (400225048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.2` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:24986c0c6f2afd743e595f38f6c95dc67b10160e4b59d0abedc87690e431eb59
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **798.0 MB (798010701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f382cc1c458fc19541123fb8183361a0636498c451182b4413774137ec15bf`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:27 GMT
ADD file:ea38b381ee92d0c4b34697af5b78def83b881e6837b309e1f41a14bee2ff2b7e in / 
# Tue, 21 Nov 2023 06:27:27 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:00:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:00:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:01:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:18 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 08:21:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 08:21:25 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 08:21:28 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 08:32:50 GMT
ARG GHC=9.2.8
# Tue, 21 Nov 2023 08:32:50 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 21 Nov 2023 08:34:14 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.8 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='645433359d8ad9e7b286f85ef5111db1b787ee3712c24c5dfde7c62769aa59a4';             ;;         'x86_64')             GHC_SHA256='10d1be25487bcf99ac8eb77beaa220c85e69f8c1106f4219ce019206ecc0ac51';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 08:34:28 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 08:34:28 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:357c576c57e480da5e7eb018506db51d822da9f357c02a76f7c4da1ccaa61b33`  
		Last Modified: Tue, 21 Nov 2023 06:31:24 GMT  
		Size: 49.3 MB (49291145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9750a1d4e9cc8d118fb8f247658f2e931026ab641d4ebdc3c3806b3dd8ee4d0d`  
		Last Modified: Tue, 21 Nov 2023 08:07:51 GMT  
		Size: 17.5 MB (17454097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55295586deeb07a4153f5f4d0cd2723a2240e52697d6ad85612c498057c0d832`  
		Last Modified: Tue, 21 Nov 2023 08:08:06 GMT  
		Size: 52.2 MB (52207152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fb9e461a1bbc28daea6d98c6425175d5ec238091b9c6d22306c3d257de50cd`  
		Last Modified: Tue, 21 Nov 2023 08:08:31 GMT  
		Size: 183.5 MB (183476090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8520593e4d4d8289c877a174b696c2830f14eb2b1b3a3a832ad50cb64aa23049`  
		Last Modified: Tue, 21 Nov 2023 08:39:07 GMT  
		Size: 517.3 KB (517300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234bbe5f5278dc328477465898a776d8addb6172cfc0ae55d199f015a74987c`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 17.2 MB (17230042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ed20186e4d0efa5eec675e66c421203c5fe383a529511ab58816cb659b96a0`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 12.4 MB (12373189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d61b87c5b0c3176bf8eab7491f393662aacefdd88a6d405a6e7d9ee2af0f195`  
		Last Modified: Tue, 21 Nov 2023 08:47:40 GMT  
		Size: 465.5 MB (465461686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.2-buster`

```console
$ docker pull haskell@sha256:c4bd03e247cd0c39c700990bb42f6e347006e0ebcb8e1358b4ac4262b64ea26d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.2-buster` - linux; amd64

```console
$ docker pull haskell@sha256:bad6b18e695d9e6e2f73443c60a3ad19c8d74273217a63bd744ad6d82ac53114
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **735.8 MB (735806049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:626f75b9d7f657f06c6201ba4e43ea28a791918b358363d483f062ac11c0354e`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:08 GMT
ADD file:4f8b7a35280160ec5a55323fa07ac91e294c86e2ea647ba212053983ef380bcf in / 
# Tue, 21 Nov 2023 05:22:08 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:55:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:56:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:57:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:47 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:39:51 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:39:55 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:39:58 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:51:39 GMT
ARG GHC=9.2.8
# Tue, 21 Nov 2023 12:51:40 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 21 Nov 2023 12:52:51 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.8 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='645433359d8ad9e7b286f85ef5111db1b787ee3712c24c5dfde7c62769aa59a4';             ;;         'x86_64')             GHC_SHA256='10d1be25487bcf99ac8eb77beaa220c85e69f8c1106f4219ce019206ecc0ac51';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:52:58 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:52:58 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b32028968d56a86ac35eac062e7abba276c547ab175fb057973c469eb41db55b`  
		Last Modified: Tue, 21 Nov 2023 05:26:57 GMT  
		Size: 50.5 MB (50499471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24c059838ae87ccefc35d50177e4e280a9e6f2f54127456ad0eaa5be5ed5386`  
		Last Modified: Tue, 21 Nov 2023 10:03:28 GMT  
		Size: 17.6 MB (17583860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819458a39dea8d30616a22068e79bcb7743745aa8b0d35fdb762ba69d98e3ec0`  
		Last Modified: Tue, 21 Nov 2023 10:03:45 GMT  
		Size: 51.9 MB (51874180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedd23d9034d9de62653c3bb2a2ca71fb88a1c6d17f386c0bfe4ac5bf8163929`  
		Last Modified: Tue, 21 Nov 2023 10:04:21 GMT  
		Size: 191.9 MB (191910019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ef9a56930d28877c2fa90904a7be44f1f8cca3356383b7f74682c75d8d994`  
		Last Modified: Tue, 21 Nov 2023 12:57:42 GMT  
		Size: 515.2 KB (515154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a1f56bfe415e8ae3055b472ce7df60a5bdf1033339c4dd235e31d400eb34c3`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 15.4 MB (15359949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35eecb76c7d0d3257ad0d1322fa0f70fe5bb08f73cd35791e40dedfeb7df855e`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f0eeefb5db658b0a0a28b275aba9c98ec4c18cfc690c89bea3da6890017a35`  
		Last Modified: Tue, 21 Nov 2023 13:06:47 GMT  
		Size: 400.2 MB (400225048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.2-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:24986c0c6f2afd743e595f38f6c95dc67b10160e4b59d0abedc87690e431eb59
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **798.0 MB (798010701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f382cc1c458fc19541123fb8183361a0636498c451182b4413774137ec15bf`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:27 GMT
ADD file:ea38b381ee92d0c4b34697af5b78def83b881e6837b309e1f41a14bee2ff2b7e in / 
# Tue, 21 Nov 2023 06:27:27 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:00:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:00:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:01:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:18 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 08:21:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 08:21:25 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 08:21:28 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 08:32:50 GMT
ARG GHC=9.2.8
# Tue, 21 Nov 2023 08:32:50 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 21 Nov 2023 08:34:14 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.8 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='645433359d8ad9e7b286f85ef5111db1b787ee3712c24c5dfde7c62769aa59a4';             ;;         'x86_64')             GHC_SHA256='10d1be25487bcf99ac8eb77beaa220c85e69f8c1106f4219ce019206ecc0ac51';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 08:34:28 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 08:34:28 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:357c576c57e480da5e7eb018506db51d822da9f357c02a76f7c4da1ccaa61b33`  
		Last Modified: Tue, 21 Nov 2023 06:31:24 GMT  
		Size: 49.3 MB (49291145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9750a1d4e9cc8d118fb8f247658f2e931026ab641d4ebdc3c3806b3dd8ee4d0d`  
		Last Modified: Tue, 21 Nov 2023 08:07:51 GMT  
		Size: 17.5 MB (17454097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55295586deeb07a4153f5f4d0cd2723a2240e52697d6ad85612c498057c0d832`  
		Last Modified: Tue, 21 Nov 2023 08:08:06 GMT  
		Size: 52.2 MB (52207152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fb9e461a1bbc28daea6d98c6425175d5ec238091b9c6d22306c3d257de50cd`  
		Last Modified: Tue, 21 Nov 2023 08:08:31 GMT  
		Size: 183.5 MB (183476090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8520593e4d4d8289c877a174b696c2830f14eb2b1b3a3a832ad50cb64aa23049`  
		Last Modified: Tue, 21 Nov 2023 08:39:07 GMT  
		Size: 517.3 KB (517300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234bbe5f5278dc328477465898a776d8addb6172cfc0ae55d199f015a74987c`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 17.2 MB (17230042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ed20186e4d0efa5eec675e66c421203c5fe383a529511ab58816cb659b96a0`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 12.4 MB (12373189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d61b87c5b0c3176bf8eab7491f393662aacefdd88a6d405a6e7d9ee2af0f195`  
		Last Modified: Tue, 21 Nov 2023 08:47:40 GMT  
		Size: 465.5 MB (465461686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.2-slim`

```console
$ docker pull haskell@sha256:f32ed1915fdd335909fca03fb26aac98f422c37fd8e8535e1228e7ca4e005dfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.2-slim` - linux; amd64

```console
$ docker pull haskell@sha256:dc522bd933134a810d6e79db53447383b9d0d7b53d0fe17f72da7bb6e448dbac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.4 MB (422396449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e9346b610dbcdba39f276085980bdac0f016ca45053b04413f3b999492a1857`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:20 GMT
ADD file:7672eb709be933bb0edec47b8141cd2ebff266a770dfae1278205f7cee43c71a in / 
# Tue, 21 Nov 2023 05:22:20 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:41:56 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:42:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:42:21 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:42:24 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:53:03 GMT
ARG GHC=9.2.8
# Tue, 21 Nov 2023 12:53:03 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 21 Nov 2023 12:54:13 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.8 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='645433359d8ad9e7b286f85ef5111db1b787ee3712c24c5dfde7c62769aa59a4';             ;;         'x86_64')             GHC_SHA256='10d1be25487bcf99ac8eb77beaa220c85e69f8c1106f4219ce019206ecc0ac51';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:54:19 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:54:19 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0fc9206bc4affb32fe13185a20b8184271c753e9b7cb81484bf770054fc69737`  
		Last Modified: Tue, 21 Nov 2023 05:27:19 GMT  
		Size: 27.2 MB (27187457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6213b4299e71dcc2c16c339ec043da12cc47384caa53a9f15259996652e6bf4`  
		Last Modified: Tue, 21 Nov 2023 12:59:36 GMT  
		Size: 94.0 MB (94045021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19344eacbd857e0b61cb66092db6d11c467aed149978f45a1dcdb057ebb9980`  
		Last Modified: Tue, 21 Nov 2023 12:59:24 GMT  
		Size: 15.4 MB (15359960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefb56630c3948901bac3dd75868f7d017f4b46579498b8fdf054347f3db9894`  
		Last Modified: Tue, 21 Nov 2023 12:59:23 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812d48ac9da115dd5157b8340769568a80093f5b46a377392954aa3b1732797b`  
		Last Modified: Tue, 21 Nov 2023 13:07:54 GMT  
		Size: 278.0 MB (277965643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.2-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:b955057dc6ae6093b9c66bdde4422de0f1e9e46dbefcb38dd57d07dfd84538c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.8 MB (463814692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d009f137f46d7515efc4964d4ad2c3051491a52bd8f15380694abd55727e169`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:39 GMT
ADD file:f60673c303a98b4e4c676e3403bc1b7cb316335aba1202205188176810494c07 in / 
# Tue, 19 Dec 2023 01:41:40 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:46:03 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 02:46:21 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK=2.11.1
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 19 Dec 2023 02:46:31 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 19 Dec 2023 02:46:34 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 19 Dec 2023 02:51:47 GMT
ARG GHC=9.2.8
# Tue, 19 Dec 2023 02:51:47 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 19 Dec 2023 02:53:04 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.8 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='645433359d8ad9e7b286f85ef5111db1b787ee3712c24c5dfde7c62769aa59a4';             ;;         'x86_64')             GHC_SHA256='10d1be25487bcf99ac8eb77beaa220c85e69f8c1106f4219ce019206ecc0ac51';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 19 Dec 2023 02:53:16 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 02:53:16 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c0b0171eefd1c6d7f85c54d4a609269c9b5e19a0fd8cd787a49c808c6b73cf74`  
		Last Modified: Tue, 19 Dec 2023 01:46:01 GMT  
		Size: 26.0 MB (25969827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6ed82599775f9bbd4cc3c5df2ebf7342daaa490b970568c1ea375e3242ebc4`  
		Last Modified: Tue, 19 Dec 2023 02:55:11 GMT  
		Size: 88.1 MB (88053431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a99edfe152899f2001989c0e6103ad6f2276cf961df3dbb4aceefec5312d373`  
		Last Modified: Tue, 19 Dec 2023 02:55:02 GMT  
		Size: 17.2 MB (17230056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20252565f8094ddee6562ad5f30ebc81e720ba92b526c0174372c3fad25e8625`  
		Last Modified: Tue, 19 Dec 2023 02:55:01 GMT  
		Size: 12.4 MB (12373194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06e745b0cd9b9f8337b1233ec1c5dd9fc0123a1ce1f1fadf178e3eea047580b`  
		Last Modified: Tue, 19 Dec 2023 02:58:55 GMT  
		Size: 320.2 MB (320188184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.2-slim-buster`

```console
$ docker pull haskell@sha256:f32ed1915fdd335909fca03fb26aac98f422c37fd8e8535e1228e7ca4e005dfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.2-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:dc522bd933134a810d6e79db53447383b9d0d7b53d0fe17f72da7bb6e448dbac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.4 MB (422396449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e9346b610dbcdba39f276085980bdac0f016ca45053b04413f3b999492a1857`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:20 GMT
ADD file:7672eb709be933bb0edec47b8141cd2ebff266a770dfae1278205f7cee43c71a in / 
# Tue, 21 Nov 2023 05:22:20 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:41:56 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:42:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:42:21 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:42:24 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:53:03 GMT
ARG GHC=9.2.8
# Tue, 21 Nov 2023 12:53:03 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 21 Nov 2023 12:54:13 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.8 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='645433359d8ad9e7b286f85ef5111db1b787ee3712c24c5dfde7c62769aa59a4';             ;;         'x86_64')             GHC_SHA256='10d1be25487bcf99ac8eb77beaa220c85e69f8c1106f4219ce019206ecc0ac51';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:54:19 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:54:19 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0fc9206bc4affb32fe13185a20b8184271c753e9b7cb81484bf770054fc69737`  
		Last Modified: Tue, 21 Nov 2023 05:27:19 GMT  
		Size: 27.2 MB (27187457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6213b4299e71dcc2c16c339ec043da12cc47384caa53a9f15259996652e6bf4`  
		Last Modified: Tue, 21 Nov 2023 12:59:36 GMT  
		Size: 94.0 MB (94045021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19344eacbd857e0b61cb66092db6d11c467aed149978f45a1dcdb057ebb9980`  
		Last Modified: Tue, 21 Nov 2023 12:59:24 GMT  
		Size: 15.4 MB (15359960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefb56630c3948901bac3dd75868f7d017f4b46579498b8fdf054347f3db9894`  
		Last Modified: Tue, 21 Nov 2023 12:59:23 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812d48ac9da115dd5157b8340769568a80093f5b46a377392954aa3b1732797b`  
		Last Modified: Tue, 21 Nov 2023 13:07:54 GMT  
		Size: 278.0 MB (277965643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.2-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:b955057dc6ae6093b9c66bdde4422de0f1e9e46dbefcb38dd57d07dfd84538c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.8 MB (463814692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d009f137f46d7515efc4964d4ad2c3051491a52bd8f15380694abd55727e169`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:39 GMT
ADD file:f60673c303a98b4e4c676e3403bc1b7cb316335aba1202205188176810494c07 in / 
# Tue, 19 Dec 2023 01:41:40 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:46:03 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 02:46:21 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK=2.11.1
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 19 Dec 2023 02:46:31 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 19 Dec 2023 02:46:34 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 19 Dec 2023 02:51:47 GMT
ARG GHC=9.2.8
# Tue, 19 Dec 2023 02:51:47 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 19 Dec 2023 02:53:04 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.8 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='645433359d8ad9e7b286f85ef5111db1b787ee3712c24c5dfde7c62769aa59a4';             ;;         'x86_64')             GHC_SHA256='10d1be25487bcf99ac8eb77beaa220c85e69f8c1106f4219ce019206ecc0ac51';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 19 Dec 2023 02:53:16 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 02:53:16 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c0b0171eefd1c6d7f85c54d4a609269c9b5e19a0fd8cd787a49c808c6b73cf74`  
		Last Modified: Tue, 19 Dec 2023 01:46:01 GMT  
		Size: 26.0 MB (25969827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6ed82599775f9bbd4cc3c5df2ebf7342daaa490b970568c1ea375e3242ebc4`  
		Last Modified: Tue, 19 Dec 2023 02:55:11 GMT  
		Size: 88.1 MB (88053431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a99edfe152899f2001989c0e6103ad6f2276cf961df3dbb4aceefec5312d373`  
		Last Modified: Tue, 19 Dec 2023 02:55:02 GMT  
		Size: 17.2 MB (17230056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20252565f8094ddee6562ad5f30ebc81e720ba92b526c0174372c3fad25e8625`  
		Last Modified: Tue, 19 Dec 2023 02:55:01 GMT  
		Size: 12.4 MB (12373194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06e745b0cd9b9f8337b1233ec1c5dd9fc0123a1ce1f1fadf178e3eea047580b`  
		Last Modified: Tue, 19 Dec 2023 02:58:55 GMT  
		Size: 320.2 MB (320188184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.2.8`

```console
$ docker pull haskell@sha256:c4bd03e247cd0c39c700990bb42f6e347006e0ebcb8e1358b4ac4262b64ea26d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.2.8` - linux; amd64

```console
$ docker pull haskell@sha256:bad6b18e695d9e6e2f73443c60a3ad19c8d74273217a63bd744ad6d82ac53114
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **735.8 MB (735806049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:626f75b9d7f657f06c6201ba4e43ea28a791918b358363d483f062ac11c0354e`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:08 GMT
ADD file:4f8b7a35280160ec5a55323fa07ac91e294c86e2ea647ba212053983ef380bcf in / 
# Tue, 21 Nov 2023 05:22:08 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:55:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:56:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:57:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:47 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:39:51 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:39:55 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:39:58 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:51:39 GMT
ARG GHC=9.2.8
# Tue, 21 Nov 2023 12:51:40 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 21 Nov 2023 12:52:51 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.8 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='645433359d8ad9e7b286f85ef5111db1b787ee3712c24c5dfde7c62769aa59a4';             ;;         'x86_64')             GHC_SHA256='10d1be25487bcf99ac8eb77beaa220c85e69f8c1106f4219ce019206ecc0ac51';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:52:58 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:52:58 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b32028968d56a86ac35eac062e7abba276c547ab175fb057973c469eb41db55b`  
		Last Modified: Tue, 21 Nov 2023 05:26:57 GMT  
		Size: 50.5 MB (50499471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24c059838ae87ccefc35d50177e4e280a9e6f2f54127456ad0eaa5be5ed5386`  
		Last Modified: Tue, 21 Nov 2023 10:03:28 GMT  
		Size: 17.6 MB (17583860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819458a39dea8d30616a22068e79bcb7743745aa8b0d35fdb762ba69d98e3ec0`  
		Last Modified: Tue, 21 Nov 2023 10:03:45 GMT  
		Size: 51.9 MB (51874180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedd23d9034d9de62653c3bb2a2ca71fb88a1c6d17f386c0bfe4ac5bf8163929`  
		Last Modified: Tue, 21 Nov 2023 10:04:21 GMT  
		Size: 191.9 MB (191910019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ef9a56930d28877c2fa90904a7be44f1f8cca3356383b7f74682c75d8d994`  
		Last Modified: Tue, 21 Nov 2023 12:57:42 GMT  
		Size: 515.2 KB (515154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a1f56bfe415e8ae3055b472ce7df60a5bdf1033339c4dd235e31d400eb34c3`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 15.4 MB (15359949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35eecb76c7d0d3257ad0d1322fa0f70fe5bb08f73cd35791e40dedfeb7df855e`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f0eeefb5db658b0a0a28b275aba9c98ec4c18cfc690c89bea3da6890017a35`  
		Last Modified: Tue, 21 Nov 2023 13:06:47 GMT  
		Size: 400.2 MB (400225048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.2.8` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:24986c0c6f2afd743e595f38f6c95dc67b10160e4b59d0abedc87690e431eb59
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **798.0 MB (798010701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f382cc1c458fc19541123fb8183361a0636498c451182b4413774137ec15bf`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:27 GMT
ADD file:ea38b381ee92d0c4b34697af5b78def83b881e6837b309e1f41a14bee2ff2b7e in / 
# Tue, 21 Nov 2023 06:27:27 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:00:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:00:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:01:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:18 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 08:21:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 08:21:25 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 08:21:28 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 08:32:50 GMT
ARG GHC=9.2.8
# Tue, 21 Nov 2023 08:32:50 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 21 Nov 2023 08:34:14 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.8 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='645433359d8ad9e7b286f85ef5111db1b787ee3712c24c5dfde7c62769aa59a4';             ;;         'x86_64')             GHC_SHA256='10d1be25487bcf99ac8eb77beaa220c85e69f8c1106f4219ce019206ecc0ac51';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 08:34:28 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 08:34:28 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:357c576c57e480da5e7eb018506db51d822da9f357c02a76f7c4da1ccaa61b33`  
		Last Modified: Tue, 21 Nov 2023 06:31:24 GMT  
		Size: 49.3 MB (49291145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9750a1d4e9cc8d118fb8f247658f2e931026ab641d4ebdc3c3806b3dd8ee4d0d`  
		Last Modified: Tue, 21 Nov 2023 08:07:51 GMT  
		Size: 17.5 MB (17454097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55295586deeb07a4153f5f4d0cd2723a2240e52697d6ad85612c498057c0d832`  
		Last Modified: Tue, 21 Nov 2023 08:08:06 GMT  
		Size: 52.2 MB (52207152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fb9e461a1bbc28daea6d98c6425175d5ec238091b9c6d22306c3d257de50cd`  
		Last Modified: Tue, 21 Nov 2023 08:08:31 GMT  
		Size: 183.5 MB (183476090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8520593e4d4d8289c877a174b696c2830f14eb2b1b3a3a832ad50cb64aa23049`  
		Last Modified: Tue, 21 Nov 2023 08:39:07 GMT  
		Size: 517.3 KB (517300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234bbe5f5278dc328477465898a776d8addb6172cfc0ae55d199f015a74987c`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 17.2 MB (17230042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ed20186e4d0efa5eec675e66c421203c5fe383a529511ab58816cb659b96a0`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 12.4 MB (12373189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d61b87c5b0c3176bf8eab7491f393662aacefdd88a6d405a6e7d9ee2af0f195`  
		Last Modified: Tue, 21 Nov 2023 08:47:40 GMT  
		Size: 465.5 MB (465461686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.2.8-buster`

```console
$ docker pull haskell@sha256:c4bd03e247cd0c39c700990bb42f6e347006e0ebcb8e1358b4ac4262b64ea26d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.2.8-buster` - linux; amd64

```console
$ docker pull haskell@sha256:bad6b18e695d9e6e2f73443c60a3ad19c8d74273217a63bd744ad6d82ac53114
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **735.8 MB (735806049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:626f75b9d7f657f06c6201ba4e43ea28a791918b358363d483f062ac11c0354e`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:08 GMT
ADD file:4f8b7a35280160ec5a55323fa07ac91e294c86e2ea647ba212053983ef380bcf in / 
# Tue, 21 Nov 2023 05:22:08 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:55:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:56:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:57:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:47 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:39:51 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:39:55 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:39:58 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:51:39 GMT
ARG GHC=9.2.8
# Tue, 21 Nov 2023 12:51:40 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 21 Nov 2023 12:52:51 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.8 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='645433359d8ad9e7b286f85ef5111db1b787ee3712c24c5dfde7c62769aa59a4';             ;;         'x86_64')             GHC_SHA256='10d1be25487bcf99ac8eb77beaa220c85e69f8c1106f4219ce019206ecc0ac51';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:52:58 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:52:58 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b32028968d56a86ac35eac062e7abba276c547ab175fb057973c469eb41db55b`  
		Last Modified: Tue, 21 Nov 2023 05:26:57 GMT  
		Size: 50.5 MB (50499471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24c059838ae87ccefc35d50177e4e280a9e6f2f54127456ad0eaa5be5ed5386`  
		Last Modified: Tue, 21 Nov 2023 10:03:28 GMT  
		Size: 17.6 MB (17583860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819458a39dea8d30616a22068e79bcb7743745aa8b0d35fdb762ba69d98e3ec0`  
		Last Modified: Tue, 21 Nov 2023 10:03:45 GMT  
		Size: 51.9 MB (51874180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedd23d9034d9de62653c3bb2a2ca71fb88a1c6d17f386c0bfe4ac5bf8163929`  
		Last Modified: Tue, 21 Nov 2023 10:04:21 GMT  
		Size: 191.9 MB (191910019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ef9a56930d28877c2fa90904a7be44f1f8cca3356383b7f74682c75d8d994`  
		Last Modified: Tue, 21 Nov 2023 12:57:42 GMT  
		Size: 515.2 KB (515154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a1f56bfe415e8ae3055b472ce7df60a5bdf1033339c4dd235e31d400eb34c3`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 15.4 MB (15359949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35eecb76c7d0d3257ad0d1322fa0f70fe5bb08f73cd35791e40dedfeb7df855e`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f0eeefb5db658b0a0a28b275aba9c98ec4c18cfc690c89bea3da6890017a35`  
		Last Modified: Tue, 21 Nov 2023 13:06:47 GMT  
		Size: 400.2 MB (400225048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.2.8-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:24986c0c6f2afd743e595f38f6c95dc67b10160e4b59d0abedc87690e431eb59
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **798.0 MB (798010701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f382cc1c458fc19541123fb8183361a0636498c451182b4413774137ec15bf`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:27 GMT
ADD file:ea38b381ee92d0c4b34697af5b78def83b881e6837b309e1f41a14bee2ff2b7e in / 
# Tue, 21 Nov 2023 06:27:27 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:00:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:00:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:01:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:18 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 08:21:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 08:21:25 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 08:21:28 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 08:32:50 GMT
ARG GHC=9.2.8
# Tue, 21 Nov 2023 08:32:50 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 21 Nov 2023 08:34:14 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.8 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='645433359d8ad9e7b286f85ef5111db1b787ee3712c24c5dfde7c62769aa59a4';             ;;         'x86_64')             GHC_SHA256='10d1be25487bcf99ac8eb77beaa220c85e69f8c1106f4219ce019206ecc0ac51';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 08:34:28 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 08:34:28 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:357c576c57e480da5e7eb018506db51d822da9f357c02a76f7c4da1ccaa61b33`  
		Last Modified: Tue, 21 Nov 2023 06:31:24 GMT  
		Size: 49.3 MB (49291145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9750a1d4e9cc8d118fb8f247658f2e931026ab641d4ebdc3c3806b3dd8ee4d0d`  
		Last Modified: Tue, 21 Nov 2023 08:07:51 GMT  
		Size: 17.5 MB (17454097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55295586deeb07a4153f5f4d0cd2723a2240e52697d6ad85612c498057c0d832`  
		Last Modified: Tue, 21 Nov 2023 08:08:06 GMT  
		Size: 52.2 MB (52207152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fb9e461a1bbc28daea6d98c6425175d5ec238091b9c6d22306c3d257de50cd`  
		Last Modified: Tue, 21 Nov 2023 08:08:31 GMT  
		Size: 183.5 MB (183476090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8520593e4d4d8289c877a174b696c2830f14eb2b1b3a3a832ad50cb64aa23049`  
		Last Modified: Tue, 21 Nov 2023 08:39:07 GMT  
		Size: 517.3 KB (517300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234bbe5f5278dc328477465898a776d8addb6172cfc0ae55d199f015a74987c`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 17.2 MB (17230042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ed20186e4d0efa5eec675e66c421203c5fe383a529511ab58816cb659b96a0`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 12.4 MB (12373189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d61b87c5b0c3176bf8eab7491f393662aacefdd88a6d405a6e7d9ee2af0f195`  
		Last Modified: Tue, 21 Nov 2023 08:47:40 GMT  
		Size: 465.5 MB (465461686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.2.8-slim`

```console
$ docker pull haskell@sha256:f32ed1915fdd335909fca03fb26aac98f422c37fd8e8535e1228e7ca4e005dfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.2.8-slim` - linux; amd64

```console
$ docker pull haskell@sha256:dc522bd933134a810d6e79db53447383b9d0d7b53d0fe17f72da7bb6e448dbac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.4 MB (422396449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e9346b610dbcdba39f276085980bdac0f016ca45053b04413f3b999492a1857`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:20 GMT
ADD file:7672eb709be933bb0edec47b8141cd2ebff266a770dfae1278205f7cee43c71a in / 
# Tue, 21 Nov 2023 05:22:20 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:41:56 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:42:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:42:21 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:42:24 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:53:03 GMT
ARG GHC=9.2.8
# Tue, 21 Nov 2023 12:53:03 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 21 Nov 2023 12:54:13 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.8 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='645433359d8ad9e7b286f85ef5111db1b787ee3712c24c5dfde7c62769aa59a4';             ;;         'x86_64')             GHC_SHA256='10d1be25487bcf99ac8eb77beaa220c85e69f8c1106f4219ce019206ecc0ac51';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:54:19 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:54:19 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0fc9206bc4affb32fe13185a20b8184271c753e9b7cb81484bf770054fc69737`  
		Last Modified: Tue, 21 Nov 2023 05:27:19 GMT  
		Size: 27.2 MB (27187457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6213b4299e71dcc2c16c339ec043da12cc47384caa53a9f15259996652e6bf4`  
		Last Modified: Tue, 21 Nov 2023 12:59:36 GMT  
		Size: 94.0 MB (94045021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19344eacbd857e0b61cb66092db6d11c467aed149978f45a1dcdb057ebb9980`  
		Last Modified: Tue, 21 Nov 2023 12:59:24 GMT  
		Size: 15.4 MB (15359960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefb56630c3948901bac3dd75868f7d017f4b46579498b8fdf054347f3db9894`  
		Last Modified: Tue, 21 Nov 2023 12:59:23 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812d48ac9da115dd5157b8340769568a80093f5b46a377392954aa3b1732797b`  
		Last Modified: Tue, 21 Nov 2023 13:07:54 GMT  
		Size: 278.0 MB (277965643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.2.8-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:b955057dc6ae6093b9c66bdde4422de0f1e9e46dbefcb38dd57d07dfd84538c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.8 MB (463814692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d009f137f46d7515efc4964d4ad2c3051491a52bd8f15380694abd55727e169`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:39 GMT
ADD file:f60673c303a98b4e4c676e3403bc1b7cb316335aba1202205188176810494c07 in / 
# Tue, 19 Dec 2023 01:41:40 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:46:03 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 02:46:21 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK=2.11.1
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 19 Dec 2023 02:46:31 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 19 Dec 2023 02:46:34 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 19 Dec 2023 02:51:47 GMT
ARG GHC=9.2.8
# Tue, 19 Dec 2023 02:51:47 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 19 Dec 2023 02:53:04 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.8 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='645433359d8ad9e7b286f85ef5111db1b787ee3712c24c5dfde7c62769aa59a4';             ;;         'x86_64')             GHC_SHA256='10d1be25487bcf99ac8eb77beaa220c85e69f8c1106f4219ce019206ecc0ac51';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 19 Dec 2023 02:53:16 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 02:53:16 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c0b0171eefd1c6d7f85c54d4a609269c9b5e19a0fd8cd787a49c808c6b73cf74`  
		Last Modified: Tue, 19 Dec 2023 01:46:01 GMT  
		Size: 26.0 MB (25969827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6ed82599775f9bbd4cc3c5df2ebf7342daaa490b970568c1ea375e3242ebc4`  
		Last Modified: Tue, 19 Dec 2023 02:55:11 GMT  
		Size: 88.1 MB (88053431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a99edfe152899f2001989c0e6103ad6f2276cf961df3dbb4aceefec5312d373`  
		Last Modified: Tue, 19 Dec 2023 02:55:02 GMT  
		Size: 17.2 MB (17230056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20252565f8094ddee6562ad5f30ebc81e720ba92b526c0174372c3fad25e8625`  
		Last Modified: Tue, 19 Dec 2023 02:55:01 GMT  
		Size: 12.4 MB (12373194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06e745b0cd9b9f8337b1233ec1c5dd9fc0123a1ce1f1fadf178e3eea047580b`  
		Last Modified: Tue, 19 Dec 2023 02:58:55 GMT  
		Size: 320.2 MB (320188184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.2.8-slim-buster`

```console
$ docker pull haskell@sha256:f32ed1915fdd335909fca03fb26aac98f422c37fd8e8535e1228e7ca4e005dfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.2.8-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:dc522bd933134a810d6e79db53447383b9d0d7b53d0fe17f72da7bb6e448dbac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.4 MB (422396449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e9346b610dbcdba39f276085980bdac0f016ca45053b04413f3b999492a1857`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:20 GMT
ADD file:7672eb709be933bb0edec47b8141cd2ebff266a770dfae1278205f7cee43c71a in / 
# Tue, 21 Nov 2023 05:22:20 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:41:56 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:42:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:42:21 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:42:24 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:53:03 GMT
ARG GHC=9.2.8
# Tue, 21 Nov 2023 12:53:03 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 21 Nov 2023 12:54:13 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.8 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='645433359d8ad9e7b286f85ef5111db1b787ee3712c24c5dfde7c62769aa59a4';             ;;         'x86_64')             GHC_SHA256='10d1be25487bcf99ac8eb77beaa220c85e69f8c1106f4219ce019206ecc0ac51';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:54:19 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:54:19 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0fc9206bc4affb32fe13185a20b8184271c753e9b7cb81484bf770054fc69737`  
		Last Modified: Tue, 21 Nov 2023 05:27:19 GMT  
		Size: 27.2 MB (27187457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6213b4299e71dcc2c16c339ec043da12cc47384caa53a9f15259996652e6bf4`  
		Last Modified: Tue, 21 Nov 2023 12:59:36 GMT  
		Size: 94.0 MB (94045021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19344eacbd857e0b61cb66092db6d11c467aed149978f45a1dcdb057ebb9980`  
		Last Modified: Tue, 21 Nov 2023 12:59:24 GMT  
		Size: 15.4 MB (15359960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefb56630c3948901bac3dd75868f7d017f4b46579498b8fdf054347f3db9894`  
		Last Modified: Tue, 21 Nov 2023 12:59:23 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812d48ac9da115dd5157b8340769568a80093f5b46a377392954aa3b1732797b`  
		Last Modified: Tue, 21 Nov 2023 13:07:54 GMT  
		Size: 278.0 MB (277965643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.2.8-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:b955057dc6ae6093b9c66bdde4422de0f1e9e46dbefcb38dd57d07dfd84538c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.8 MB (463814692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d009f137f46d7515efc4964d4ad2c3051491a52bd8f15380694abd55727e169`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:39 GMT
ADD file:f60673c303a98b4e4c676e3403bc1b7cb316335aba1202205188176810494c07 in / 
# Tue, 19 Dec 2023 01:41:40 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:46:03 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 02:46:21 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK=2.11.1
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 19 Dec 2023 02:46:31 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 19 Dec 2023 02:46:34 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 19 Dec 2023 02:51:47 GMT
ARG GHC=9.2.8
# Tue, 19 Dec 2023 02:51:47 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 19 Dec 2023 02:53:04 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.8 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='645433359d8ad9e7b286f85ef5111db1b787ee3712c24c5dfde7c62769aa59a4';             ;;         'x86_64')             GHC_SHA256='10d1be25487bcf99ac8eb77beaa220c85e69f8c1106f4219ce019206ecc0ac51';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 19 Dec 2023 02:53:16 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 02:53:16 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c0b0171eefd1c6d7f85c54d4a609269c9b5e19a0fd8cd787a49c808c6b73cf74`  
		Last Modified: Tue, 19 Dec 2023 01:46:01 GMT  
		Size: 26.0 MB (25969827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6ed82599775f9bbd4cc3c5df2ebf7342daaa490b970568c1ea375e3242ebc4`  
		Last Modified: Tue, 19 Dec 2023 02:55:11 GMT  
		Size: 88.1 MB (88053431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a99edfe152899f2001989c0e6103ad6f2276cf961df3dbb4aceefec5312d373`  
		Last Modified: Tue, 19 Dec 2023 02:55:02 GMT  
		Size: 17.2 MB (17230056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20252565f8094ddee6562ad5f30ebc81e720ba92b526c0174372c3fad25e8625`  
		Last Modified: Tue, 19 Dec 2023 02:55:01 GMT  
		Size: 12.4 MB (12373194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f06e745b0cd9b9f8337b1233ec1c5dd9fc0123a1ce1f1fadf178e3eea047580b`  
		Last Modified: Tue, 19 Dec 2023 02:58:55 GMT  
		Size: 320.2 MB (320188184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.4`

```console
$ docker pull haskell@sha256:4236af2f9f8d97903db797f7b8f149d6b65440a0d7fd147a51f637acc254e6ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.4` - linux; amd64

```console
$ docker pull haskell@sha256:cb35dc67c5aece4b5739acbcafd57792fabe09f37e06545c07fa0e2af33e468a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **763.7 MB (763689052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0786a9eb628bdbad4a54662fb56007772629f0fa934a7942675772392d632e0c`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:08 GMT
ADD file:4f8b7a35280160ec5a55323fa07ac91e294c86e2ea647ba212053983ef380bcf in / 
# Tue, 21 Nov 2023 05:22:08 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:55:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:56:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:57:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:47 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:39:51 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:39:55 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:39:58 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:48:07 GMT
ARG GHC=9.4.8
# Tue, 21 Nov 2023 12:48:07 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Tue, 21 Nov 2023 12:49:37 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.8 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='278e287e1ee624712b9c6d7803d1cf915ca1cce56e013b0a16215eb8dfeb1531';             ;;         'x86_64')             GHC_SHA256='fc77eaae5b89f29177bf159fd95ce438066ec64a46bf69df61b267102afdb10e';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:49:44 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:49:44 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b32028968d56a86ac35eac062e7abba276c547ab175fb057973c469eb41db55b`  
		Last Modified: Tue, 21 Nov 2023 05:26:57 GMT  
		Size: 50.5 MB (50499471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24c059838ae87ccefc35d50177e4e280a9e6f2f54127456ad0eaa5be5ed5386`  
		Last Modified: Tue, 21 Nov 2023 10:03:28 GMT  
		Size: 17.6 MB (17583860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819458a39dea8d30616a22068e79bcb7743745aa8b0d35fdb762ba69d98e3ec0`  
		Last Modified: Tue, 21 Nov 2023 10:03:45 GMT  
		Size: 51.9 MB (51874180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedd23d9034d9de62653c3bb2a2ca71fb88a1c6d17f386c0bfe4ac5bf8163929`  
		Last Modified: Tue, 21 Nov 2023 10:04:21 GMT  
		Size: 191.9 MB (191910019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ef9a56930d28877c2fa90904a7be44f1f8cca3356383b7f74682c75d8d994`  
		Last Modified: Tue, 21 Nov 2023 12:57:42 GMT  
		Size: 515.2 KB (515154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a1f56bfe415e8ae3055b472ce7df60a5bdf1033339c4dd235e31d400eb34c3`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 15.4 MB (15359949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35eecb76c7d0d3257ad0d1322fa0f70fe5bb08f73cd35791e40dedfeb7df855e`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200cead9bc6475fdf33ee0fbae5ad1d54ba3373f8dc77360e5bee397ae10c3e5`  
		Last Modified: Tue, 21 Nov 2023 13:04:19 GMT  
		Size: 428.1 MB (428108051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.4` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:832a6576a8160484e91f8b623c0aae898809f247532f27dc3971de73c9026d1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **809.7 MB (809696447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34199e40a5b9aed76cdf104fe34ac131a96d1b5b000007d48119e397876a227c`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:27 GMT
ADD file:ea38b381ee92d0c4b34697af5b78def83b881e6837b309e1f41a14bee2ff2b7e in / 
# Tue, 21 Nov 2023 06:27:27 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:00:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:00:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:01:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:18 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 08:21:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 08:21:25 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 08:21:28 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 08:29:20 GMT
ARG GHC=9.4.8
# Tue, 21 Nov 2023 08:29:20 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Tue, 21 Nov 2023 08:30:50 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.8 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='278e287e1ee624712b9c6d7803d1cf915ca1cce56e013b0a16215eb8dfeb1531';             ;;         'x86_64')             GHC_SHA256='fc77eaae5b89f29177bf159fd95ce438066ec64a46bf69df61b267102afdb10e';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 08:31:03 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 08:31:03 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:357c576c57e480da5e7eb018506db51d822da9f357c02a76f7c4da1ccaa61b33`  
		Last Modified: Tue, 21 Nov 2023 06:31:24 GMT  
		Size: 49.3 MB (49291145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9750a1d4e9cc8d118fb8f247658f2e931026ab641d4ebdc3c3806b3dd8ee4d0d`  
		Last Modified: Tue, 21 Nov 2023 08:07:51 GMT  
		Size: 17.5 MB (17454097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55295586deeb07a4153f5f4d0cd2723a2240e52697d6ad85612c498057c0d832`  
		Last Modified: Tue, 21 Nov 2023 08:08:06 GMT  
		Size: 52.2 MB (52207152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fb9e461a1bbc28daea6d98c6425175d5ec238091b9c6d22306c3d257de50cd`  
		Last Modified: Tue, 21 Nov 2023 08:08:31 GMT  
		Size: 183.5 MB (183476090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8520593e4d4d8289c877a174b696c2830f14eb2b1b3a3a832ad50cb64aa23049`  
		Last Modified: Tue, 21 Nov 2023 08:39:07 GMT  
		Size: 517.3 KB (517300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234bbe5f5278dc328477465898a776d8addb6172cfc0ae55d199f015a74987c`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 17.2 MB (17230042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ed20186e4d0efa5eec675e66c421203c5fe383a529511ab58816cb659b96a0`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 12.4 MB (12373189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de489a3bfd9199f3a469c7b0cc1fa53ecc4bedc7b30e741ec86545d9538fde3`  
		Last Modified: Tue, 21 Nov 2023 08:45:09 GMT  
		Size: 477.1 MB (477147432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.4-buster`

```console
$ docker pull haskell@sha256:4236af2f9f8d97903db797f7b8f149d6b65440a0d7fd147a51f637acc254e6ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.4-buster` - linux; amd64

```console
$ docker pull haskell@sha256:cb35dc67c5aece4b5739acbcafd57792fabe09f37e06545c07fa0e2af33e468a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **763.7 MB (763689052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0786a9eb628bdbad4a54662fb56007772629f0fa934a7942675772392d632e0c`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:08 GMT
ADD file:4f8b7a35280160ec5a55323fa07ac91e294c86e2ea647ba212053983ef380bcf in / 
# Tue, 21 Nov 2023 05:22:08 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:55:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:56:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:57:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:47 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:39:51 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:39:55 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:39:58 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:48:07 GMT
ARG GHC=9.4.8
# Tue, 21 Nov 2023 12:48:07 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Tue, 21 Nov 2023 12:49:37 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.8 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='278e287e1ee624712b9c6d7803d1cf915ca1cce56e013b0a16215eb8dfeb1531';             ;;         'x86_64')             GHC_SHA256='fc77eaae5b89f29177bf159fd95ce438066ec64a46bf69df61b267102afdb10e';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:49:44 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:49:44 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b32028968d56a86ac35eac062e7abba276c547ab175fb057973c469eb41db55b`  
		Last Modified: Tue, 21 Nov 2023 05:26:57 GMT  
		Size: 50.5 MB (50499471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24c059838ae87ccefc35d50177e4e280a9e6f2f54127456ad0eaa5be5ed5386`  
		Last Modified: Tue, 21 Nov 2023 10:03:28 GMT  
		Size: 17.6 MB (17583860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819458a39dea8d30616a22068e79bcb7743745aa8b0d35fdb762ba69d98e3ec0`  
		Last Modified: Tue, 21 Nov 2023 10:03:45 GMT  
		Size: 51.9 MB (51874180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedd23d9034d9de62653c3bb2a2ca71fb88a1c6d17f386c0bfe4ac5bf8163929`  
		Last Modified: Tue, 21 Nov 2023 10:04:21 GMT  
		Size: 191.9 MB (191910019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ef9a56930d28877c2fa90904a7be44f1f8cca3356383b7f74682c75d8d994`  
		Last Modified: Tue, 21 Nov 2023 12:57:42 GMT  
		Size: 515.2 KB (515154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a1f56bfe415e8ae3055b472ce7df60a5bdf1033339c4dd235e31d400eb34c3`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 15.4 MB (15359949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35eecb76c7d0d3257ad0d1322fa0f70fe5bb08f73cd35791e40dedfeb7df855e`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200cead9bc6475fdf33ee0fbae5ad1d54ba3373f8dc77360e5bee397ae10c3e5`  
		Last Modified: Tue, 21 Nov 2023 13:04:19 GMT  
		Size: 428.1 MB (428108051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.4-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:832a6576a8160484e91f8b623c0aae898809f247532f27dc3971de73c9026d1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **809.7 MB (809696447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34199e40a5b9aed76cdf104fe34ac131a96d1b5b000007d48119e397876a227c`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:27 GMT
ADD file:ea38b381ee92d0c4b34697af5b78def83b881e6837b309e1f41a14bee2ff2b7e in / 
# Tue, 21 Nov 2023 06:27:27 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:00:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:00:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:01:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:18 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 08:21:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 08:21:25 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 08:21:28 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 08:29:20 GMT
ARG GHC=9.4.8
# Tue, 21 Nov 2023 08:29:20 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Tue, 21 Nov 2023 08:30:50 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.8 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='278e287e1ee624712b9c6d7803d1cf915ca1cce56e013b0a16215eb8dfeb1531';             ;;         'x86_64')             GHC_SHA256='fc77eaae5b89f29177bf159fd95ce438066ec64a46bf69df61b267102afdb10e';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 08:31:03 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 08:31:03 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:357c576c57e480da5e7eb018506db51d822da9f357c02a76f7c4da1ccaa61b33`  
		Last Modified: Tue, 21 Nov 2023 06:31:24 GMT  
		Size: 49.3 MB (49291145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9750a1d4e9cc8d118fb8f247658f2e931026ab641d4ebdc3c3806b3dd8ee4d0d`  
		Last Modified: Tue, 21 Nov 2023 08:07:51 GMT  
		Size: 17.5 MB (17454097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55295586deeb07a4153f5f4d0cd2723a2240e52697d6ad85612c498057c0d832`  
		Last Modified: Tue, 21 Nov 2023 08:08:06 GMT  
		Size: 52.2 MB (52207152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fb9e461a1bbc28daea6d98c6425175d5ec238091b9c6d22306c3d257de50cd`  
		Last Modified: Tue, 21 Nov 2023 08:08:31 GMT  
		Size: 183.5 MB (183476090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8520593e4d4d8289c877a174b696c2830f14eb2b1b3a3a832ad50cb64aa23049`  
		Last Modified: Tue, 21 Nov 2023 08:39:07 GMT  
		Size: 517.3 KB (517300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234bbe5f5278dc328477465898a776d8addb6172cfc0ae55d199f015a74987c`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 17.2 MB (17230042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ed20186e4d0efa5eec675e66c421203c5fe383a529511ab58816cb659b96a0`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 12.4 MB (12373189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de489a3bfd9199f3a469c7b0cc1fa53ecc4bedc7b30e741ec86545d9538fde3`  
		Last Modified: Tue, 21 Nov 2023 08:45:09 GMT  
		Size: 477.1 MB (477147432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.4-slim`

```console
$ docker pull haskell@sha256:fe9dc9a0d481473a0675143c90a9be4f7994cafb7b05a6861e4251ac038c5191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.4-slim` - linux; amd64

```console
$ docker pull haskell@sha256:9a071b67c087906d58441e8725801caee188ec63016bc0948e01c3bcdb0830ee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.0 MB (429992442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f7e37ae849c259ba2c246f860f1afabc609dd123b7ff2958e79fb559050bb0a`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:20 GMT
ADD file:7672eb709be933bb0edec47b8141cd2ebff266a770dfae1278205f7cee43c71a in / 
# Tue, 21 Nov 2023 05:22:20 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:41:56 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:42:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:42:21 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:42:24 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:50:01 GMT
ARG GHC=9.4.8
# Tue, 21 Nov 2023 12:50:01 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Tue, 21 Nov 2023 12:51:25 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.8 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='278e287e1ee624712b9c6d7803d1cf915ca1cce56e013b0a16215eb8dfeb1531';             ;;         'x86_64')             GHC_SHA256='fc77eaae5b89f29177bf159fd95ce438066ec64a46bf69df61b267102afdb10e';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:51:30 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:51:30 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0fc9206bc4affb32fe13185a20b8184271c753e9b7cb81484bf770054fc69737`  
		Last Modified: Tue, 21 Nov 2023 05:27:19 GMT  
		Size: 27.2 MB (27187457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6213b4299e71dcc2c16c339ec043da12cc47384caa53a9f15259996652e6bf4`  
		Last Modified: Tue, 21 Nov 2023 12:59:36 GMT  
		Size: 94.0 MB (94045021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19344eacbd857e0b61cb66092db6d11c467aed149978f45a1dcdb057ebb9980`  
		Last Modified: Tue, 21 Nov 2023 12:59:24 GMT  
		Size: 15.4 MB (15359960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefb56630c3948901bac3dd75868f7d017f4b46579498b8fdf054347f3db9894`  
		Last Modified: Tue, 21 Nov 2023 12:59:23 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed722ef810d0b23cfac647d0cf7630864b60055c062e6ee81db0f9644c0595d3`  
		Last Modified: Tue, 21 Nov 2023 13:05:19 GMT  
		Size: 285.6 MB (285561636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.4-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:387c10a0c8d314f664045b0c65f41e4a466fd719d99b1a5bcbeacd9bdb4d16aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **454.4 MB (454364205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04d9089364f460a6f7a6e9f7b9d9d60712a45c31ea443dcab03d5dc75734e320`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:39 GMT
ADD file:f60673c303a98b4e4c676e3403bc1b7cb316335aba1202205188176810494c07 in / 
# Tue, 19 Dec 2023 01:41:40 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:46:03 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 02:46:21 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK=2.11.1
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 19 Dec 2023 02:46:31 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 19 Dec 2023 02:46:34 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 19 Dec 2023 02:50:07 GMT
ARG GHC=9.4.8
# Tue, 19 Dec 2023 02:50:07 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Tue, 19 Dec 2023 02:51:30 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.8 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='278e287e1ee624712b9c6d7803d1cf915ca1cce56e013b0a16215eb8dfeb1531';             ;;         'x86_64')             GHC_SHA256='fc77eaae5b89f29177bf159fd95ce438066ec64a46bf69df61b267102afdb10e';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 19 Dec 2023 02:51:41 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 02:51:42 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c0b0171eefd1c6d7f85c54d4a609269c9b5e19a0fd8cd787a49c808c6b73cf74`  
		Last Modified: Tue, 19 Dec 2023 01:46:01 GMT  
		Size: 26.0 MB (25969827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6ed82599775f9bbd4cc3c5df2ebf7342daaa490b970568c1ea375e3242ebc4`  
		Last Modified: Tue, 19 Dec 2023 02:55:11 GMT  
		Size: 88.1 MB (88053431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a99edfe152899f2001989c0e6103ad6f2276cf961df3dbb4aceefec5312d373`  
		Last Modified: Tue, 19 Dec 2023 02:55:02 GMT  
		Size: 17.2 MB (17230056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20252565f8094ddee6562ad5f30ebc81e720ba92b526c0174372c3fad25e8625`  
		Last Modified: Tue, 19 Dec 2023 02:55:01 GMT  
		Size: 12.4 MB (12373194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51870f40c1a2dab11b51e6c8a2b293e6b508f34a0eb236d30c60a2f73c9dd726`  
		Last Modified: Tue, 19 Dec 2023 02:57:48 GMT  
		Size: 310.7 MB (310737697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.4-slim-buster`

```console
$ docker pull haskell@sha256:fe9dc9a0d481473a0675143c90a9be4f7994cafb7b05a6861e4251ac038c5191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.4-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:9a071b67c087906d58441e8725801caee188ec63016bc0948e01c3bcdb0830ee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.0 MB (429992442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f7e37ae849c259ba2c246f860f1afabc609dd123b7ff2958e79fb559050bb0a`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:20 GMT
ADD file:7672eb709be933bb0edec47b8141cd2ebff266a770dfae1278205f7cee43c71a in / 
# Tue, 21 Nov 2023 05:22:20 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:41:56 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:42:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:42:21 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:42:24 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:50:01 GMT
ARG GHC=9.4.8
# Tue, 21 Nov 2023 12:50:01 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Tue, 21 Nov 2023 12:51:25 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.8 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='278e287e1ee624712b9c6d7803d1cf915ca1cce56e013b0a16215eb8dfeb1531';             ;;         'x86_64')             GHC_SHA256='fc77eaae5b89f29177bf159fd95ce438066ec64a46bf69df61b267102afdb10e';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:51:30 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:51:30 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0fc9206bc4affb32fe13185a20b8184271c753e9b7cb81484bf770054fc69737`  
		Last Modified: Tue, 21 Nov 2023 05:27:19 GMT  
		Size: 27.2 MB (27187457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6213b4299e71dcc2c16c339ec043da12cc47384caa53a9f15259996652e6bf4`  
		Last Modified: Tue, 21 Nov 2023 12:59:36 GMT  
		Size: 94.0 MB (94045021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19344eacbd857e0b61cb66092db6d11c467aed149978f45a1dcdb057ebb9980`  
		Last Modified: Tue, 21 Nov 2023 12:59:24 GMT  
		Size: 15.4 MB (15359960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefb56630c3948901bac3dd75868f7d017f4b46579498b8fdf054347f3db9894`  
		Last Modified: Tue, 21 Nov 2023 12:59:23 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed722ef810d0b23cfac647d0cf7630864b60055c062e6ee81db0f9644c0595d3`  
		Last Modified: Tue, 21 Nov 2023 13:05:19 GMT  
		Size: 285.6 MB (285561636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.4-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:387c10a0c8d314f664045b0c65f41e4a466fd719d99b1a5bcbeacd9bdb4d16aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **454.4 MB (454364205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04d9089364f460a6f7a6e9f7b9d9d60712a45c31ea443dcab03d5dc75734e320`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:39 GMT
ADD file:f60673c303a98b4e4c676e3403bc1b7cb316335aba1202205188176810494c07 in / 
# Tue, 19 Dec 2023 01:41:40 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:46:03 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 02:46:21 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK=2.11.1
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 19 Dec 2023 02:46:31 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 19 Dec 2023 02:46:34 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 19 Dec 2023 02:50:07 GMT
ARG GHC=9.4.8
# Tue, 19 Dec 2023 02:50:07 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Tue, 19 Dec 2023 02:51:30 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.8 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='278e287e1ee624712b9c6d7803d1cf915ca1cce56e013b0a16215eb8dfeb1531';             ;;         'x86_64')             GHC_SHA256='fc77eaae5b89f29177bf159fd95ce438066ec64a46bf69df61b267102afdb10e';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 19 Dec 2023 02:51:41 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 02:51:42 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c0b0171eefd1c6d7f85c54d4a609269c9b5e19a0fd8cd787a49c808c6b73cf74`  
		Last Modified: Tue, 19 Dec 2023 01:46:01 GMT  
		Size: 26.0 MB (25969827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6ed82599775f9bbd4cc3c5df2ebf7342daaa490b970568c1ea375e3242ebc4`  
		Last Modified: Tue, 19 Dec 2023 02:55:11 GMT  
		Size: 88.1 MB (88053431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a99edfe152899f2001989c0e6103ad6f2276cf961df3dbb4aceefec5312d373`  
		Last Modified: Tue, 19 Dec 2023 02:55:02 GMT  
		Size: 17.2 MB (17230056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20252565f8094ddee6562ad5f30ebc81e720ba92b526c0174372c3fad25e8625`  
		Last Modified: Tue, 19 Dec 2023 02:55:01 GMT  
		Size: 12.4 MB (12373194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51870f40c1a2dab11b51e6c8a2b293e6b508f34a0eb236d30c60a2f73c9dd726`  
		Last Modified: Tue, 19 Dec 2023 02:57:48 GMT  
		Size: 310.7 MB (310737697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.4.8`

```console
$ docker pull haskell@sha256:4236af2f9f8d97903db797f7b8f149d6b65440a0d7fd147a51f637acc254e6ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.4.8` - linux; amd64

```console
$ docker pull haskell@sha256:cb35dc67c5aece4b5739acbcafd57792fabe09f37e06545c07fa0e2af33e468a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **763.7 MB (763689052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0786a9eb628bdbad4a54662fb56007772629f0fa934a7942675772392d632e0c`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:08 GMT
ADD file:4f8b7a35280160ec5a55323fa07ac91e294c86e2ea647ba212053983ef380bcf in / 
# Tue, 21 Nov 2023 05:22:08 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:55:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:56:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:57:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:47 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:39:51 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:39:55 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:39:58 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:48:07 GMT
ARG GHC=9.4.8
# Tue, 21 Nov 2023 12:48:07 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Tue, 21 Nov 2023 12:49:37 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.8 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='278e287e1ee624712b9c6d7803d1cf915ca1cce56e013b0a16215eb8dfeb1531';             ;;         'x86_64')             GHC_SHA256='fc77eaae5b89f29177bf159fd95ce438066ec64a46bf69df61b267102afdb10e';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:49:44 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:49:44 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b32028968d56a86ac35eac062e7abba276c547ab175fb057973c469eb41db55b`  
		Last Modified: Tue, 21 Nov 2023 05:26:57 GMT  
		Size: 50.5 MB (50499471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24c059838ae87ccefc35d50177e4e280a9e6f2f54127456ad0eaa5be5ed5386`  
		Last Modified: Tue, 21 Nov 2023 10:03:28 GMT  
		Size: 17.6 MB (17583860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819458a39dea8d30616a22068e79bcb7743745aa8b0d35fdb762ba69d98e3ec0`  
		Last Modified: Tue, 21 Nov 2023 10:03:45 GMT  
		Size: 51.9 MB (51874180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedd23d9034d9de62653c3bb2a2ca71fb88a1c6d17f386c0bfe4ac5bf8163929`  
		Last Modified: Tue, 21 Nov 2023 10:04:21 GMT  
		Size: 191.9 MB (191910019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ef9a56930d28877c2fa90904a7be44f1f8cca3356383b7f74682c75d8d994`  
		Last Modified: Tue, 21 Nov 2023 12:57:42 GMT  
		Size: 515.2 KB (515154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a1f56bfe415e8ae3055b472ce7df60a5bdf1033339c4dd235e31d400eb34c3`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 15.4 MB (15359949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35eecb76c7d0d3257ad0d1322fa0f70fe5bb08f73cd35791e40dedfeb7df855e`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200cead9bc6475fdf33ee0fbae5ad1d54ba3373f8dc77360e5bee397ae10c3e5`  
		Last Modified: Tue, 21 Nov 2023 13:04:19 GMT  
		Size: 428.1 MB (428108051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.4.8` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:832a6576a8160484e91f8b623c0aae898809f247532f27dc3971de73c9026d1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **809.7 MB (809696447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34199e40a5b9aed76cdf104fe34ac131a96d1b5b000007d48119e397876a227c`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:27 GMT
ADD file:ea38b381ee92d0c4b34697af5b78def83b881e6837b309e1f41a14bee2ff2b7e in / 
# Tue, 21 Nov 2023 06:27:27 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:00:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:00:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:01:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:18 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 08:21:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 08:21:25 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 08:21:28 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 08:29:20 GMT
ARG GHC=9.4.8
# Tue, 21 Nov 2023 08:29:20 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Tue, 21 Nov 2023 08:30:50 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.8 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='278e287e1ee624712b9c6d7803d1cf915ca1cce56e013b0a16215eb8dfeb1531';             ;;         'x86_64')             GHC_SHA256='fc77eaae5b89f29177bf159fd95ce438066ec64a46bf69df61b267102afdb10e';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 08:31:03 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 08:31:03 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:357c576c57e480da5e7eb018506db51d822da9f357c02a76f7c4da1ccaa61b33`  
		Last Modified: Tue, 21 Nov 2023 06:31:24 GMT  
		Size: 49.3 MB (49291145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9750a1d4e9cc8d118fb8f247658f2e931026ab641d4ebdc3c3806b3dd8ee4d0d`  
		Last Modified: Tue, 21 Nov 2023 08:07:51 GMT  
		Size: 17.5 MB (17454097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55295586deeb07a4153f5f4d0cd2723a2240e52697d6ad85612c498057c0d832`  
		Last Modified: Tue, 21 Nov 2023 08:08:06 GMT  
		Size: 52.2 MB (52207152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fb9e461a1bbc28daea6d98c6425175d5ec238091b9c6d22306c3d257de50cd`  
		Last Modified: Tue, 21 Nov 2023 08:08:31 GMT  
		Size: 183.5 MB (183476090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8520593e4d4d8289c877a174b696c2830f14eb2b1b3a3a832ad50cb64aa23049`  
		Last Modified: Tue, 21 Nov 2023 08:39:07 GMT  
		Size: 517.3 KB (517300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234bbe5f5278dc328477465898a776d8addb6172cfc0ae55d199f015a74987c`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 17.2 MB (17230042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ed20186e4d0efa5eec675e66c421203c5fe383a529511ab58816cb659b96a0`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 12.4 MB (12373189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de489a3bfd9199f3a469c7b0cc1fa53ecc4bedc7b30e741ec86545d9538fde3`  
		Last Modified: Tue, 21 Nov 2023 08:45:09 GMT  
		Size: 477.1 MB (477147432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.4.8-buster`

```console
$ docker pull haskell@sha256:4236af2f9f8d97903db797f7b8f149d6b65440a0d7fd147a51f637acc254e6ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.4.8-buster` - linux; amd64

```console
$ docker pull haskell@sha256:cb35dc67c5aece4b5739acbcafd57792fabe09f37e06545c07fa0e2af33e468a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **763.7 MB (763689052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0786a9eb628bdbad4a54662fb56007772629f0fa934a7942675772392d632e0c`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:08 GMT
ADD file:4f8b7a35280160ec5a55323fa07ac91e294c86e2ea647ba212053983ef380bcf in / 
# Tue, 21 Nov 2023 05:22:08 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:55:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:56:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:57:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:47 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:39:51 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:39:55 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:39:58 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:48:07 GMT
ARG GHC=9.4.8
# Tue, 21 Nov 2023 12:48:07 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Tue, 21 Nov 2023 12:49:37 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.8 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='278e287e1ee624712b9c6d7803d1cf915ca1cce56e013b0a16215eb8dfeb1531';             ;;         'x86_64')             GHC_SHA256='fc77eaae5b89f29177bf159fd95ce438066ec64a46bf69df61b267102afdb10e';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:49:44 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:49:44 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b32028968d56a86ac35eac062e7abba276c547ab175fb057973c469eb41db55b`  
		Last Modified: Tue, 21 Nov 2023 05:26:57 GMT  
		Size: 50.5 MB (50499471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24c059838ae87ccefc35d50177e4e280a9e6f2f54127456ad0eaa5be5ed5386`  
		Last Modified: Tue, 21 Nov 2023 10:03:28 GMT  
		Size: 17.6 MB (17583860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819458a39dea8d30616a22068e79bcb7743745aa8b0d35fdb762ba69d98e3ec0`  
		Last Modified: Tue, 21 Nov 2023 10:03:45 GMT  
		Size: 51.9 MB (51874180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedd23d9034d9de62653c3bb2a2ca71fb88a1c6d17f386c0bfe4ac5bf8163929`  
		Last Modified: Tue, 21 Nov 2023 10:04:21 GMT  
		Size: 191.9 MB (191910019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ef9a56930d28877c2fa90904a7be44f1f8cca3356383b7f74682c75d8d994`  
		Last Modified: Tue, 21 Nov 2023 12:57:42 GMT  
		Size: 515.2 KB (515154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a1f56bfe415e8ae3055b472ce7df60a5bdf1033339c4dd235e31d400eb34c3`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 15.4 MB (15359949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35eecb76c7d0d3257ad0d1322fa0f70fe5bb08f73cd35791e40dedfeb7df855e`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200cead9bc6475fdf33ee0fbae5ad1d54ba3373f8dc77360e5bee397ae10c3e5`  
		Last Modified: Tue, 21 Nov 2023 13:04:19 GMT  
		Size: 428.1 MB (428108051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.4.8-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:832a6576a8160484e91f8b623c0aae898809f247532f27dc3971de73c9026d1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **809.7 MB (809696447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34199e40a5b9aed76cdf104fe34ac131a96d1b5b000007d48119e397876a227c`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:27 GMT
ADD file:ea38b381ee92d0c4b34697af5b78def83b881e6837b309e1f41a14bee2ff2b7e in / 
# Tue, 21 Nov 2023 06:27:27 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:00:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:00:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:01:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:18 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 08:21:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 08:21:25 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 08:21:28 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 08:29:20 GMT
ARG GHC=9.4.8
# Tue, 21 Nov 2023 08:29:20 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Tue, 21 Nov 2023 08:30:50 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.8 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='278e287e1ee624712b9c6d7803d1cf915ca1cce56e013b0a16215eb8dfeb1531';             ;;         'x86_64')             GHC_SHA256='fc77eaae5b89f29177bf159fd95ce438066ec64a46bf69df61b267102afdb10e';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 08:31:03 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 08:31:03 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:357c576c57e480da5e7eb018506db51d822da9f357c02a76f7c4da1ccaa61b33`  
		Last Modified: Tue, 21 Nov 2023 06:31:24 GMT  
		Size: 49.3 MB (49291145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9750a1d4e9cc8d118fb8f247658f2e931026ab641d4ebdc3c3806b3dd8ee4d0d`  
		Last Modified: Tue, 21 Nov 2023 08:07:51 GMT  
		Size: 17.5 MB (17454097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55295586deeb07a4153f5f4d0cd2723a2240e52697d6ad85612c498057c0d832`  
		Last Modified: Tue, 21 Nov 2023 08:08:06 GMT  
		Size: 52.2 MB (52207152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fb9e461a1bbc28daea6d98c6425175d5ec238091b9c6d22306c3d257de50cd`  
		Last Modified: Tue, 21 Nov 2023 08:08:31 GMT  
		Size: 183.5 MB (183476090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8520593e4d4d8289c877a174b696c2830f14eb2b1b3a3a832ad50cb64aa23049`  
		Last Modified: Tue, 21 Nov 2023 08:39:07 GMT  
		Size: 517.3 KB (517300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234bbe5f5278dc328477465898a776d8addb6172cfc0ae55d199f015a74987c`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 17.2 MB (17230042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ed20186e4d0efa5eec675e66c421203c5fe383a529511ab58816cb659b96a0`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 12.4 MB (12373189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de489a3bfd9199f3a469c7b0cc1fa53ecc4bedc7b30e741ec86545d9538fde3`  
		Last Modified: Tue, 21 Nov 2023 08:45:09 GMT  
		Size: 477.1 MB (477147432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.4.8-slim`

```console
$ docker pull haskell@sha256:fe9dc9a0d481473a0675143c90a9be4f7994cafb7b05a6861e4251ac038c5191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.4.8-slim` - linux; amd64

```console
$ docker pull haskell@sha256:9a071b67c087906d58441e8725801caee188ec63016bc0948e01c3bcdb0830ee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.0 MB (429992442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f7e37ae849c259ba2c246f860f1afabc609dd123b7ff2958e79fb559050bb0a`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:20 GMT
ADD file:7672eb709be933bb0edec47b8141cd2ebff266a770dfae1278205f7cee43c71a in / 
# Tue, 21 Nov 2023 05:22:20 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:41:56 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:42:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:42:21 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:42:24 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:50:01 GMT
ARG GHC=9.4.8
# Tue, 21 Nov 2023 12:50:01 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Tue, 21 Nov 2023 12:51:25 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.8 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='278e287e1ee624712b9c6d7803d1cf915ca1cce56e013b0a16215eb8dfeb1531';             ;;         'x86_64')             GHC_SHA256='fc77eaae5b89f29177bf159fd95ce438066ec64a46bf69df61b267102afdb10e';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:51:30 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:51:30 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0fc9206bc4affb32fe13185a20b8184271c753e9b7cb81484bf770054fc69737`  
		Last Modified: Tue, 21 Nov 2023 05:27:19 GMT  
		Size: 27.2 MB (27187457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6213b4299e71dcc2c16c339ec043da12cc47384caa53a9f15259996652e6bf4`  
		Last Modified: Tue, 21 Nov 2023 12:59:36 GMT  
		Size: 94.0 MB (94045021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19344eacbd857e0b61cb66092db6d11c467aed149978f45a1dcdb057ebb9980`  
		Last Modified: Tue, 21 Nov 2023 12:59:24 GMT  
		Size: 15.4 MB (15359960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefb56630c3948901bac3dd75868f7d017f4b46579498b8fdf054347f3db9894`  
		Last Modified: Tue, 21 Nov 2023 12:59:23 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed722ef810d0b23cfac647d0cf7630864b60055c062e6ee81db0f9644c0595d3`  
		Last Modified: Tue, 21 Nov 2023 13:05:19 GMT  
		Size: 285.6 MB (285561636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.4.8-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:387c10a0c8d314f664045b0c65f41e4a466fd719d99b1a5bcbeacd9bdb4d16aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **454.4 MB (454364205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04d9089364f460a6f7a6e9f7b9d9d60712a45c31ea443dcab03d5dc75734e320`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:39 GMT
ADD file:f60673c303a98b4e4c676e3403bc1b7cb316335aba1202205188176810494c07 in / 
# Tue, 19 Dec 2023 01:41:40 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:46:03 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 02:46:21 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK=2.11.1
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 19 Dec 2023 02:46:31 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 19 Dec 2023 02:46:34 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 19 Dec 2023 02:50:07 GMT
ARG GHC=9.4.8
# Tue, 19 Dec 2023 02:50:07 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Tue, 19 Dec 2023 02:51:30 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.8 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='278e287e1ee624712b9c6d7803d1cf915ca1cce56e013b0a16215eb8dfeb1531';             ;;         'x86_64')             GHC_SHA256='fc77eaae5b89f29177bf159fd95ce438066ec64a46bf69df61b267102afdb10e';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 19 Dec 2023 02:51:41 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 02:51:42 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c0b0171eefd1c6d7f85c54d4a609269c9b5e19a0fd8cd787a49c808c6b73cf74`  
		Last Modified: Tue, 19 Dec 2023 01:46:01 GMT  
		Size: 26.0 MB (25969827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6ed82599775f9bbd4cc3c5df2ebf7342daaa490b970568c1ea375e3242ebc4`  
		Last Modified: Tue, 19 Dec 2023 02:55:11 GMT  
		Size: 88.1 MB (88053431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a99edfe152899f2001989c0e6103ad6f2276cf961df3dbb4aceefec5312d373`  
		Last Modified: Tue, 19 Dec 2023 02:55:02 GMT  
		Size: 17.2 MB (17230056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20252565f8094ddee6562ad5f30ebc81e720ba92b526c0174372c3fad25e8625`  
		Last Modified: Tue, 19 Dec 2023 02:55:01 GMT  
		Size: 12.4 MB (12373194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51870f40c1a2dab11b51e6c8a2b293e6b508f34a0eb236d30c60a2f73c9dd726`  
		Last Modified: Tue, 19 Dec 2023 02:57:48 GMT  
		Size: 310.7 MB (310737697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.4.8-slim-buster`

```console
$ docker pull haskell@sha256:fe9dc9a0d481473a0675143c90a9be4f7994cafb7b05a6861e4251ac038c5191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.4.8-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:9a071b67c087906d58441e8725801caee188ec63016bc0948e01c3bcdb0830ee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.0 MB (429992442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f7e37ae849c259ba2c246f860f1afabc609dd123b7ff2958e79fb559050bb0a`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:20 GMT
ADD file:7672eb709be933bb0edec47b8141cd2ebff266a770dfae1278205f7cee43c71a in / 
# Tue, 21 Nov 2023 05:22:20 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:41:56 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:42:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:42:21 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:42:24 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:50:01 GMT
ARG GHC=9.4.8
# Tue, 21 Nov 2023 12:50:01 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Tue, 21 Nov 2023 12:51:25 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.8 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='278e287e1ee624712b9c6d7803d1cf915ca1cce56e013b0a16215eb8dfeb1531';             ;;         'x86_64')             GHC_SHA256='fc77eaae5b89f29177bf159fd95ce438066ec64a46bf69df61b267102afdb10e';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:51:30 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:51:30 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0fc9206bc4affb32fe13185a20b8184271c753e9b7cb81484bf770054fc69737`  
		Last Modified: Tue, 21 Nov 2023 05:27:19 GMT  
		Size: 27.2 MB (27187457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6213b4299e71dcc2c16c339ec043da12cc47384caa53a9f15259996652e6bf4`  
		Last Modified: Tue, 21 Nov 2023 12:59:36 GMT  
		Size: 94.0 MB (94045021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19344eacbd857e0b61cb66092db6d11c467aed149978f45a1dcdb057ebb9980`  
		Last Modified: Tue, 21 Nov 2023 12:59:24 GMT  
		Size: 15.4 MB (15359960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefb56630c3948901bac3dd75868f7d017f4b46579498b8fdf054347f3db9894`  
		Last Modified: Tue, 21 Nov 2023 12:59:23 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed722ef810d0b23cfac647d0cf7630864b60055c062e6ee81db0f9644c0595d3`  
		Last Modified: Tue, 21 Nov 2023 13:05:19 GMT  
		Size: 285.6 MB (285561636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.4.8-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:387c10a0c8d314f664045b0c65f41e4a466fd719d99b1a5bcbeacd9bdb4d16aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **454.4 MB (454364205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04d9089364f460a6f7a6e9f7b9d9d60712a45c31ea443dcab03d5dc75734e320`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:39 GMT
ADD file:f60673c303a98b4e4c676e3403bc1b7cb316335aba1202205188176810494c07 in / 
# Tue, 19 Dec 2023 01:41:40 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:46:03 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 02:46:21 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK=2.11.1
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 19 Dec 2023 02:46:31 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 19 Dec 2023 02:46:34 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 19 Dec 2023 02:50:07 GMT
ARG GHC=9.4.8
# Tue, 19 Dec 2023 02:50:07 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Tue, 19 Dec 2023 02:51:30 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.4.8 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='278e287e1ee624712b9c6d7803d1cf915ca1cce56e013b0a16215eb8dfeb1531';             ;;         'x86_64')             GHC_SHA256='fc77eaae5b89f29177bf159fd95ce438066ec64a46bf69df61b267102afdb10e';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 19 Dec 2023 02:51:41 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 02:51:42 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c0b0171eefd1c6d7f85c54d4a609269c9b5e19a0fd8cd787a49c808c6b73cf74`  
		Last Modified: Tue, 19 Dec 2023 01:46:01 GMT  
		Size: 26.0 MB (25969827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6ed82599775f9bbd4cc3c5df2ebf7342daaa490b970568c1ea375e3242ebc4`  
		Last Modified: Tue, 19 Dec 2023 02:55:11 GMT  
		Size: 88.1 MB (88053431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a99edfe152899f2001989c0e6103ad6f2276cf961df3dbb4aceefec5312d373`  
		Last Modified: Tue, 19 Dec 2023 02:55:02 GMT  
		Size: 17.2 MB (17230056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20252565f8094ddee6562ad5f30ebc81e720ba92b526c0174372c3fad25e8625`  
		Last Modified: Tue, 19 Dec 2023 02:55:01 GMT  
		Size: 12.4 MB (12373194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51870f40c1a2dab11b51e6c8a2b293e6b508f34a0eb236d30c60a2f73c9dd726`  
		Last Modified: Tue, 19 Dec 2023 02:57:48 GMT  
		Size: 310.7 MB (310737697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.6`

```console
$ docker pull haskell@sha256:fe58947d967844aa3254759de6ae5cb57aa6d8a3ef443cc260079a0a1bd34d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.6` - linux; amd64

```console
$ docker pull haskell@sha256:d911888eab111a3711b559d23498f4b8a5dcc289a96ec06d8c010dc577d8ece8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.7 MB (759742811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d4108139cc84bf1374ce605d97071e72bf4bbb69da39e37b5ddf4353e0751cb`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:08 GMT
ADD file:4f8b7a35280160ec5a55323fa07ac91e294c86e2ea647ba212053983ef380bcf in / 
# Tue, 21 Nov 2023 05:22:08 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:55:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:56:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:57:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:47 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:39:51 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:39:55 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:39:58 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:44:20 GMT
ARG GHC=9.6.3
# Tue, 21 Nov 2023 12:44:20 GMT
ARG GHC_RELEASE_KEY=33C3A599DB85EA9B8BAA1866B202264020068BFB
# Tue, 21 Nov 2023 12:45:56 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.6.3 GHC_RELEASE_KEY=33C3A599DB85EA9B8BAA1866B202264020068BFB STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='03c389859319f09452081310fc13af7525063ea8930830ef76be2a14b312271e';             ;;         'x86_64')             GHC_SHA256='9ba0458c84efdbba69509c3c57497e22ad03743f816eb9c8b024abc13f7aacaa';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:46:03 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:46:03 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b32028968d56a86ac35eac062e7abba276c547ab175fb057973c469eb41db55b`  
		Last Modified: Tue, 21 Nov 2023 05:26:57 GMT  
		Size: 50.5 MB (50499471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24c059838ae87ccefc35d50177e4e280a9e6f2f54127456ad0eaa5be5ed5386`  
		Last Modified: Tue, 21 Nov 2023 10:03:28 GMT  
		Size: 17.6 MB (17583860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819458a39dea8d30616a22068e79bcb7743745aa8b0d35fdb762ba69d98e3ec0`  
		Last Modified: Tue, 21 Nov 2023 10:03:45 GMT  
		Size: 51.9 MB (51874180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedd23d9034d9de62653c3bb2a2ca71fb88a1c6d17f386c0bfe4ac5bf8163929`  
		Last Modified: Tue, 21 Nov 2023 10:04:21 GMT  
		Size: 191.9 MB (191910019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ef9a56930d28877c2fa90904a7be44f1f8cca3356383b7f74682c75d8d994`  
		Last Modified: Tue, 21 Nov 2023 12:57:42 GMT  
		Size: 515.2 KB (515154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a1f56bfe415e8ae3055b472ce7df60a5bdf1033339c4dd235e31d400eb34c3`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 15.4 MB (15359949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35eecb76c7d0d3257ad0d1322fa0f70fe5bb08f73cd35791e40dedfeb7df855e`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0e9b73e0ca3e835463c5e23f4651e5b72818127c694134646d41ab2c0f53cd`  
		Last Modified: Tue, 21 Nov 2023 13:01:50 GMT  
		Size: 424.2 MB (424161810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.6` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:f211f3e3a61b675d7224849c02f747fe37c022c469fd84188582509b3957b57c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **764.5 MB (764458663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e217b8b7e3451643249986f60289bcfa74c199c9f6079ce3cc42c1993a21099c`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:27 GMT
ADD file:ea38b381ee92d0c4b34697af5b78def83b881e6837b309e1f41a14bee2ff2b7e in / 
# Tue, 21 Nov 2023 06:27:27 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:00:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:00:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:01:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:18 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 08:21:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 08:21:25 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 08:21:28 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 08:25:34 GMT
ARG GHC=9.6.3
# Tue, 21 Nov 2023 08:25:34 GMT
ARG GHC_RELEASE_KEY=33C3A599DB85EA9B8BAA1866B202264020068BFB
# Tue, 21 Nov 2023 08:27:02 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.6.3 GHC_RELEASE_KEY=33C3A599DB85EA9B8BAA1866B202264020068BFB STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='03c389859319f09452081310fc13af7525063ea8930830ef76be2a14b312271e';             ;;         'x86_64')             GHC_SHA256='9ba0458c84efdbba69509c3c57497e22ad03743f816eb9c8b024abc13f7aacaa';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 08:27:15 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 08:27:15 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:357c576c57e480da5e7eb018506db51d822da9f357c02a76f7c4da1ccaa61b33`  
		Last Modified: Tue, 21 Nov 2023 06:31:24 GMT  
		Size: 49.3 MB (49291145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9750a1d4e9cc8d118fb8f247658f2e931026ab641d4ebdc3c3806b3dd8ee4d0d`  
		Last Modified: Tue, 21 Nov 2023 08:07:51 GMT  
		Size: 17.5 MB (17454097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55295586deeb07a4153f5f4d0cd2723a2240e52697d6ad85612c498057c0d832`  
		Last Modified: Tue, 21 Nov 2023 08:08:06 GMT  
		Size: 52.2 MB (52207152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fb9e461a1bbc28daea6d98c6425175d5ec238091b9c6d22306c3d257de50cd`  
		Last Modified: Tue, 21 Nov 2023 08:08:31 GMT  
		Size: 183.5 MB (183476090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8520593e4d4d8289c877a174b696c2830f14eb2b1b3a3a832ad50cb64aa23049`  
		Last Modified: Tue, 21 Nov 2023 08:39:07 GMT  
		Size: 517.3 KB (517300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234bbe5f5278dc328477465898a776d8addb6172cfc0ae55d199f015a74987c`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 17.2 MB (17230042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ed20186e4d0efa5eec675e66c421203c5fe383a529511ab58816cb659b96a0`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 12.4 MB (12373189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c393754494c424e8db0ad3483bff80207f1096cce794937df0bdfd2806d4ce`  
		Last Modified: Tue, 21 Nov 2023 08:42:50 GMT  
		Size: 431.9 MB (431909648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.6-buster`

```console
$ docker pull haskell@sha256:fe58947d967844aa3254759de6ae5cb57aa6d8a3ef443cc260079a0a1bd34d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.6-buster` - linux; amd64

```console
$ docker pull haskell@sha256:d911888eab111a3711b559d23498f4b8a5dcc289a96ec06d8c010dc577d8ece8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.7 MB (759742811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d4108139cc84bf1374ce605d97071e72bf4bbb69da39e37b5ddf4353e0751cb`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:08 GMT
ADD file:4f8b7a35280160ec5a55323fa07ac91e294c86e2ea647ba212053983ef380bcf in / 
# Tue, 21 Nov 2023 05:22:08 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:55:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:56:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:57:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:47 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:39:51 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:39:55 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:39:58 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:44:20 GMT
ARG GHC=9.6.3
# Tue, 21 Nov 2023 12:44:20 GMT
ARG GHC_RELEASE_KEY=33C3A599DB85EA9B8BAA1866B202264020068BFB
# Tue, 21 Nov 2023 12:45:56 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.6.3 GHC_RELEASE_KEY=33C3A599DB85EA9B8BAA1866B202264020068BFB STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='03c389859319f09452081310fc13af7525063ea8930830ef76be2a14b312271e';             ;;         'x86_64')             GHC_SHA256='9ba0458c84efdbba69509c3c57497e22ad03743f816eb9c8b024abc13f7aacaa';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:46:03 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:46:03 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b32028968d56a86ac35eac062e7abba276c547ab175fb057973c469eb41db55b`  
		Last Modified: Tue, 21 Nov 2023 05:26:57 GMT  
		Size: 50.5 MB (50499471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24c059838ae87ccefc35d50177e4e280a9e6f2f54127456ad0eaa5be5ed5386`  
		Last Modified: Tue, 21 Nov 2023 10:03:28 GMT  
		Size: 17.6 MB (17583860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819458a39dea8d30616a22068e79bcb7743745aa8b0d35fdb762ba69d98e3ec0`  
		Last Modified: Tue, 21 Nov 2023 10:03:45 GMT  
		Size: 51.9 MB (51874180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedd23d9034d9de62653c3bb2a2ca71fb88a1c6d17f386c0bfe4ac5bf8163929`  
		Last Modified: Tue, 21 Nov 2023 10:04:21 GMT  
		Size: 191.9 MB (191910019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ef9a56930d28877c2fa90904a7be44f1f8cca3356383b7f74682c75d8d994`  
		Last Modified: Tue, 21 Nov 2023 12:57:42 GMT  
		Size: 515.2 KB (515154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a1f56bfe415e8ae3055b472ce7df60a5bdf1033339c4dd235e31d400eb34c3`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 15.4 MB (15359949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35eecb76c7d0d3257ad0d1322fa0f70fe5bb08f73cd35791e40dedfeb7df855e`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0e9b73e0ca3e835463c5e23f4651e5b72818127c694134646d41ab2c0f53cd`  
		Last Modified: Tue, 21 Nov 2023 13:01:50 GMT  
		Size: 424.2 MB (424161810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.6-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:f211f3e3a61b675d7224849c02f747fe37c022c469fd84188582509b3957b57c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **764.5 MB (764458663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e217b8b7e3451643249986f60289bcfa74c199c9f6079ce3cc42c1993a21099c`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:27 GMT
ADD file:ea38b381ee92d0c4b34697af5b78def83b881e6837b309e1f41a14bee2ff2b7e in / 
# Tue, 21 Nov 2023 06:27:27 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:00:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:00:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:01:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:18 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 08:21:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 08:21:25 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 08:21:28 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 08:25:34 GMT
ARG GHC=9.6.3
# Tue, 21 Nov 2023 08:25:34 GMT
ARG GHC_RELEASE_KEY=33C3A599DB85EA9B8BAA1866B202264020068BFB
# Tue, 21 Nov 2023 08:27:02 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.6.3 GHC_RELEASE_KEY=33C3A599DB85EA9B8BAA1866B202264020068BFB STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='03c389859319f09452081310fc13af7525063ea8930830ef76be2a14b312271e';             ;;         'x86_64')             GHC_SHA256='9ba0458c84efdbba69509c3c57497e22ad03743f816eb9c8b024abc13f7aacaa';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 08:27:15 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 08:27:15 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:357c576c57e480da5e7eb018506db51d822da9f357c02a76f7c4da1ccaa61b33`  
		Last Modified: Tue, 21 Nov 2023 06:31:24 GMT  
		Size: 49.3 MB (49291145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9750a1d4e9cc8d118fb8f247658f2e931026ab641d4ebdc3c3806b3dd8ee4d0d`  
		Last Modified: Tue, 21 Nov 2023 08:07:51 GMT  
		Size: 17.5 MB (17454097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55295586deeb07a4153f5f4d0cd2723a2240e52697d6ad85612c498057c0d832`  
		Last Modified: Tue, 21 Nov 2023 08:08:06 GMT  
		Size: 52.2 MB (52207152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fb9e461a1bbc28daea6d98c6425175d5ec238091b9c6d22306c3d257de50cd`  
		Last Modified: Tue, 21 Nov 2023 08:08:31 GMT  
		Size: 183.5 MB (183476090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8520593e4d4d8289c877a174b696c2830f14eb2b1b3a3a832ad50cb64aa23049`  
		Last Modified: Tue, 21 Nov 2023 08:39:07 GMT  
		Size: 517.3 KB (517300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234bbe5f5278dc328477465898a776d8addb6172cfc0ae55d199f015a74987c`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 17.2 MB (17230042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ed20186e4d0efa5eec675e66c421203c5fe383a529511ab58816cb659b96a0`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 12.4 MB (12373189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c393754494c424e8db0ad3483bff80207f1096cce794937df0bdfd2806d4ce`  
		Last Modified: Tue, 21 Nov 2023 08:42:50 GMT  
		Size: 431.9 MB (431909648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.6-slim`

```console
$ docker pull haskell@sha256:6a2ca8fe3d7ff3a9ace0dce72ac5c7ad562106e5a2b77bdc22ade682143cabf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.6-slim` - linux; amd64

```console
$ docker pull haskell@sha256:bb2f4fac9fd4ccbaf0b127b22aab26bafe00a78827d6ffa8a2847f7993b33bdc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.4 MB (427375116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4743189a29af3ade5951af6bc7d987310a85227b5edb930112160bb7867a507c`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:20 GMT
ADD file:7672eb709be933bb0edec47b8141cd2ebff266a770dfae1278205f7cee43c71a in / 
# Tue, 21 Nov 2023 05:22:20 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:41:56 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:42:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:42:21 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:42:24 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:46:13 GMT
ARG GHC=9.6.3
# Tue, 21 Nov 2023 12:46:13 GMT
ARG GHC_RELEASE_KEY=33C3A599DB85EA9B8BAA1866B202264020068BFB
# Tue, 21 Nov 2023 12:47:44 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.6.3 GHC_RELEASE_KEY=33C3A599DB85EA9B8BAA1866B202264020068BFB STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='03c389859319f09452081310fc13af7525063ea8930830ef76be2a14b312271e';             ;;         'x86_64')             GHC_SHA256='9ba0458c84efdbba69509c3c57497e22ad03743f816eb9c8b024abc13f7aacaa';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:47:50 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:47:50 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0fc9206bc4affb32fe13185a20b8184271c753e9b7cb81484bf770054fc69737`  
		Last Modified: Tue, 21 Nov 2023 05:27:19 GMT  
		Size: 27.2 MB (27187457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6213b4299e71dcc2c16c339ec043da12cc47384caa53a9f15259996652e6bf4`  
		Last Modified: Tue, 21 Nov 2023 12:59:36 GMT  
		Size: 94.0 MB (94045021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19344eacbd857e0b61cb66092db6d11c467aed149978f45a1dcdb057ebb9980`  
		Last Modified: Tue, 21 Nov 2023 12:59:24 GMT  
		Size: 15.4 MB (15359960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefb56630c3948901bac3dd75868f7d017f4b46579498b8fdf054347f3db9894`  
		Last Modified: Tue, 21 Nov 2023 12:59:23 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb31202f8acd4cff09dcb1643dbd5a4b9b62bf6563fe92ad9c416e8ff6d8d24a`  
		Last Modified: Tue, 21 Nov 2023 13:02:54 GMT  
		Size: 282.9 MB (282944310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.6-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:04b2c704eab0b9b5213a7cee276c5a151781707f137dff25d49273d938da03d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.7 MB (433696151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27101b331a316e834c75644567b15ff81696dd19dfa2ecec2f9250fcb1a56fff`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:39 GMT
ADD file:f60673c303a98b4e4c676e3403bc1b7cb316335aba1202205188176810494c07 in / 
# Tue, 19 Dec 2023 01:41:40 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:46:03 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 02:46:21 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK=2.11.1
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 19 Dec 2023 02:46:31 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 19 Dec 2023 02:46:34 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 19 Dec 2023 02:48:28 GMT
ARG GHC=9.6.3
# Tue, 19 Dec 2023 02:48:28 GMT
ARG GHC_RELEASE_KEY=33C3A599DB85EA9B8BAA1866B202264020068BFB
# Tue, 19 Dec 2023 02:49:48 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.6.3 GHC_RELEASE_KEY=33C3A599DB85EA9B8BAA1866B202264020068BFB STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='03c389859319f09452081310fc13af7525063ea8930830ef76be2a14b312271e';             ;;         'x86_64')             GHC_SHA256='9ba0458c84efdbba69509c3c57497e22ad03743f816eb9c8b024abc13f7aacaa';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 19 Dec 2023 02:49:58 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 02:49:58 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c0b0171eefd1c6d7f85c54d4a609269c9b5e19a0fd8cd787a49c808c6b73cf74`  
		Last Modified: Tue, 19 Dec 2023 01:46:01 GMT  
		Size: 26.0 MB (25969827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6ed82599775f9bbd4cc3c5df2ebf7342daaa490b970568c1ea375e3242ebc4`  
		Last Modified: Tue, 19 Dec 2023 02:55:11 GMT  
		Size: 88.1 MB (88053431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a99edfe152899f2001989c0e6103ad6f2276cf961df3dbb4aceefec5312d373`  
		Last Modified: Tue, 19 Dec 2023 02:55:02 GMT  
		Size: 17.2 MB (17230056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20252565f8094ddee6562ad5f30ebc81e720ba92b526c0174372c3fad25e8625`  
		Last Modified: Tue, 19 Dec 2023 02:55:01 GMT  
		Size: 12.4 MB (12373194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0df18857542919d351ed6263e743602c25e62587c8a679a4945c41fb77665af`  
		Last Modified: Tue, 19 Dec 2023 02:56:48 GMT  
		Size: 290.1 MB (290069643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.6-slim-buster`

```console
$ docker pull haskell@sha256:6a2ca8fe3d7ff3a9ace0dce72ac5c7ad562106e5a2b77bdc22ade682143cabf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.6-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:bb2f4fac9fd4ccbaf0b127b22aab26bafe00a78827d6ffa8a2847f7993b33bdc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.4 MB (427375116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4743189a29af3ade5951af6bc7d987310a85227b5edb930112160bb7867a507c`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:20 GMT
ADD file:7672eb709be933bb0edec47b8141cd2ebff266a770dfae1278205f7cee43c71a in / 
# Tue, 21 Nov 2023 05:22:20 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:41:56 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:42:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:42:21 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:42:24 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:46:13 GMT
ARG GHC=9.6.3
# Tue, 21 Nov 2023 12:46:13 GMT
ARG GHC_RELEASE_KEY=33C3A599DB85EA9B8BAA1866B202264020068BFB
# Tue, 21 Nov 2023 12:47:44 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.6.3 GHC_RELEASE_KEY=33C3A599DB85EA9B8BAA1866B202264020068BFB STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='03c389859319f09452081310fc13af7525063ea8930830ef76be2a14b312271e';             ;;         'x86_64')             GHC_SHA256='9ba0458c84efdbba69509c3c57497e22ad03743f816eb9c8b024abc13f7aacaa';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:47:50 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:47:50 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0fc9206bc4affb32fe13185a20b8184271c753e9b7cb81484bf770054fc69737`  
		Last Modified: Tue, 21 Nov 2023 05:27:19 GMT  
		Size: 27.2 MB (27187457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6213b4299e71dcc2c16c339ec043da12cc47384caa53a9f15259996652e6bf4`  
		Last Modified: Tue, 21 Nov 2023 12:59:36 GMT  
		Size: 94.0 MB (94045021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19344eacbd857e0b61cb66092db6d11c467aed149978f45a1dcdb057ebb9980`  
		Last Modified: Tue, 21 Nov 2023 12:59:24 GMT  
		Size: 15.4 MB (15359960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefb56630c3948901bac3dd75868f7d017f4b46579498b8fdf054347f3db9894`  
		Last Modified: Tue, 21 Nov 2023 12:59:23 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb31202f8acd4cff09dcb1643dbd5a4b9b62bf6563fe92ad9c416e8ff6d8d24a`  
		Last Modified: Tue, 21 Nov 2023 13:02:54 GMT  
		Size: 282.9 MB (282944310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.6-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:04b2c704eab0b9b5213a7cee276c5a151781707f137dff25d49273d938da03d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.7 MB (433696151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27101b331a316e834c75644567b15ff81696dd19dfa2ecec2f9250fcb1a56fff`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:39 GMT
ADD file:f60673c303a98b4e4c676e3403bc1b7cb316335aba1202205188176810494c07 in / 
# Tue, 19 Dec 2023 01:41:40 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:46:03 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 02:46:21 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK=2.11.1
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 19 Dec 2023 02:46:31 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 19 Dec 2023 02:46:34 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 19 Dec 2023 02:48:28 GMT
ARG GHC=9.6.3
# Tue, 19 Dec 2023 02:48:28 GMT
ARG GHC_RELEASE_KEY=33C3A599DB85EA9B8BAA1866B202264020068BFB
# Tue, 19 Dec 2023 02:49:48 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.6.3 GHC_RELEASE_KEY=33C3A599DB85EA9B8BAA1866B202264020068BFB STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='03c389859319f09452081310fc13af7525063ea8930830ef76be2a14b312271e';             ;;         'x86_64')             GHC_SHA256='9ba0458c84efdbba69509c3c57497e22ad03743f816eb9c8b024abc13f7aacaa';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 19 Dec 2023 02:49:58 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 02:49:58 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c0b0171eefd1c6d7f85c54d4a609269c9b5e19a0fd8cd787a49c808c6b73cf74`  
		Last Modified: Tue, 19 Dec 2023 01:46:01 GMT  
		Size: 26.0 MB (25969827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6ed82599775f9bbd4cc3c5df2ebf7342daaa490b970568c1ea375e3242ebc4`  
		Last Modified: Tue, 19 Dec 2023 02:55:11 GMT  
		Size: 88.1 MB (88053431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a99edfe152899f2001989c0e6103ad6f2276cf961df3dbb4aceefec5312d373`  
		Last Modified: Tue, 19 Dec 2023 02:55:02 GMT  
		Size: 17.2 MB (17230056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20252565f8094ddee6562ad5f30ebc81e720ba92b526c0174372c3fad25e8625`  
		Last Modified: Tue, 19 Dec 2023 02:55:01 GMT  
		Size: 12.4 MB (12373194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0df18857542919d351ed6263e743602c25e62587c8a679a4945c41fb77665af`  
		Last Modified: Tue, 19 Dec 2023 02:56:48 GMT  
		Size: 290.1 MB (290069643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.6.3`

```console
$ docker pull haskell@sha256:fe58947d967844aa3254759de6ae5cb57aa6d8a3ef443cc260079a0a1bd34d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.6.3` - linux; amd64

```console
$ docker pull haskell@sha256:d911888eab111a3711b559d23498f4b8a5dcc289a96ec06d8c010dc577d8ece8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.7 MB (759742811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d4108139cc84bf1374ce605d97071e72bf4bbb69da39e37b5ddf4353e0751cb`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:08 GMT
ADD file:4f8b7a35280160ec5a55323fa07ac91e294c86e2ea647ba212053983ef380bcf in / 
# Tue, 21 Nov 2023 05:22:08 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:55:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:56:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:57:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:47 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:39:51 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:39:55 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:39:58 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:44:20 GMT
ARG GHC=9.6.3
# Tue, 21 Nov 2023 12:44:20 GMT
ARG GHC_RELEASE_KEY=33C3A599DB85EA9B8BAA1866B202264020068BFB
# Tue, 21 Nov 2023 12:45:56 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.6.3 GHC_RELEASE_KEY=33C3A599DB85EA9B8BAA1866B202264020068BFB STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='03c389859319f09452081310fc13af7525063ea8930830ef76be2a14b312271e';             ;;         'x86_64')             GHC_SHA256='9ba0458c84efdbba69509c3c57497e22ad03743f816eb9c8b024abc13f7aacaa';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:46:03 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:46:03 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b32028968d56a86ac35eac062e7abba276c547ab175fb057973c469eb41db55b`  
		Last Modified: Tue, 21 Nov 2023 05:26:57 GMT  
		Size: 50.5 MB (50499471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24c059838ae87ccefc35d50177e4e280a9e6f2f54127456ad0eaa5be5ed5386`  
		Last Modified: Tue, 21 Nov 2023 10:03:28 GMT  
		Size: 17.6 MB (17583860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819458a39dea8d30616a22068e79bcb7743745aa8b0d35fdb762ba69d98e3ec0`  
		Last Modified: Tue, 21 Nov 2023 10:03:45 GMT  
		Size: 51.9 MB (51874180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedd23d9034d9de62653c3bb2a2ca71fb88a1c6d17f386c0bfe4ac5bf8163929`  
		Last Modified: Tue, 21 Nov 2023 10:04:21 GMT  
		Size: 191.9 MB (191910019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ef9a56930d28877c2fa90904a7be44f1f8cca3356383b7f74682c75d8d994`  
		Last Modified: Tue, 21 Nov 2023 12:57:42 GMT  
		Size: 515.2 KB (515154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a1f56bfe415e8ae3055b472ce7df60a5bdf1033339c4dd235e31d400eb34c3`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 15.4 MB (15359949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35eecb76c7d0d3257ad0d1322fa0f70fe5bb08f73cd35791e40dedfeb7df855e`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0e9b73e0ca3e835463c5e23f4651e5b72818127c694134646d41ab2c0f53cd`  
		Last Modified: Tue, 21 Nov 2023 13:01:50 GMT  
		Size: 424.2 MB (424161810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.6.3` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:f211f3e3a61b675d7224849c02f747fe37c022c469fd84188582509b3957b57c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **764.5 MB (764458663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e217b8b7e3451643249986f60289bcfa74c199c9f6079ce3cc42c1993a21099c`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:27 GMT
ADD file:ea38b381ee92d0c4b34697af5b78def83b881e6837b309e1f41a14bee2ff2b7e in / 
# Tue, 21 Nov 2023 06:27:27 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:00:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:00:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:01:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:18 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 08:21:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 08:21:25 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 08:21:28 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 08:25:34 GMT
ARG GHC=9.6.3
# Tue, 21 Nov 2023 08:25:34 GMT
ARG GHC_RELEASE_KEY=33C3A599DB85EA9B8BAA1866B202264020068BFB
# Tue, 21 Nov 2023 08:27:02 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.6.3 GHC_RELEASE_KEY=33C3A599DB85EA9B8BAA1866B202264020068BFB STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='03c389859319f09452081310fc13af7525063ea8930830ef76be2a14b312271e';             ;;         'x86_64')             GHC_SHA256='9ba0458c84efdbba69509c3c57497e22ad03743f816eb9c8b024abc13f7aacaa';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 08:27:15 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 08:27:15 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:357c576c57e480da5e7eb018506db51d822da9f357c02a76f7c4da1ccaa61b33`  
		Last Modified: Tue, 21 Nov 2023 06:31:24 GMT  
		Size: 49.3 MB (49291145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9750a1d4e9cc8d118fb8f247658f2e931026ab641d4ebdc3c3806b3dd8ee4d0d`  
		Last Modified: Tue, 21 Nov 2023 08:07:51 GMT  
		Size: 17.5 MB (17454097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55295586deeb07a4153f5f4d0cd2723a2240e52697d6ad85612c498057c0d832`  
		Last Modified: Tue, 21 Nov 2023 08:08:06 GMT  
		Size: 52.2 MB (52207152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fb9e461a1bbc28daea6d98c6425175d5ec238091b9c6d22306c3d257de50cd`  
		Last Modified: Tue, 21 Nov 2023 08:08:31 GMT  
		Size: 183.5 MB (183476090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8520593e4d4d8289c877a174b696c2830f14eb2b1b3a3a832ad50cb64aa23049`  
		Last Modified: Tue, 21 Nov 2023 08:39:07 GMT  
		Size: 517.3 KB (517300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234bbe5f5278dc328477465898a776d8addb6172cfc0ae55d199f015a74987c`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 17.2 MB (17230042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ed20186e4d0efa5eec675e66c421203c5fe383a529511ab58816cb659b96a0`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 12.4 MB (12373189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c393754494c424e8db0ad3483bff80207f1096cce794937df0bdfd2806d4ce`  
		Last Modified: Tue, 21 Nov 2023 08:42:50 GMT  
		Size: 431.9 MB (431909648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.6.3-buster`

```console
$ docker pull haskell@sha256:fe58947d967844aa3254759de6ae5cb57aa6d8a3ef443cc260079a0a1bd34d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.6.3-buster` - linux; amd64

```console
$ docker pull haskell@sha256:d911888eab111a3711b559d23498f4b8a5dcc289a96ec06d8c010dc577d8ece8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **759.7 MB (759742811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d4108139cc84bf1374ce605d97071e72bf4bbb69da39e37b5ddf4353e0751cb`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:08 GMT
ADD file:4f8b7a35280160ec5a55323fa07ac91e294c86e2ea647ba212053983ef380bcf in / 
# Tue, 21 Nov 2023 05:22:08 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:55:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:56:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:57:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:47 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:39:51 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:39:55 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:39:58 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:44:20 GMT
ARG GHC=9.6.3
# Tue, 21 Nov 2023 12:44:20 GMT
ARG GHC_RELEASE_KEY=33C3A599DB85EA9B8BAA1866B202264020068BFB
# Tue, 21 Nov 2023 12:45:56 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.6.3 GHC_RELEASE_KEY=33C3A599DB85EA9B8BAA1866B202264020068BFB STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='03c389859319f09452081310fc13af7525063ea8930830ef76be2a14b312271e';             ;;         'x86_64')             GHC_SHA256='9ba0458c84efdbba69509c3c57497e22ad03743f816eb9c8b024abc13f7aacaa';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:46:03 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:46:03 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b32028968d56a86ac35eac062e7abba276c547ab175fb057973c469eb41db55b`  
		Last Modified: Tue, 21 Nov 2023 05:26:57 GMT  
		Size: 50.5 MB (50499471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24c059838ae87ccefc35d50177e4e280a9e6f2f54127456ad0eaa5be5ed5386`  
		Last Modified: Tue, 21 Nov 2023 10:03:28 GMT  
		Size: 17.6 MB (17583860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819458a39dea8d30616a22068e79bcb7743745aa8b0d35fdb762ba69d98e3ec0`  
		Last Modified: Tue, 21 Nov 2023 10:03:45 GMT  
		Size: 51.9 MB (51874180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedd23d9034d9de62653c3bb2a2ca71fb88a1c6d17f386c0bfe4ac5bf8163929`  
		Last Modified: Tue, 21 Nov 2023 10:04:21 GMT  
		Size: 191.9 MB (191910019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ef9a56930d28877c2fa90904a7be44f1f8cca3356383b7f74682c75d8d994`  
		Last Modified: Tue, 21 Nov 2023 12:57:42 GMT  
		Size: 515.2 KB (515154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a1f56bfe415e8ae3055b472ce7df60a5bdf1033339c4dd235e31d400eb34c3`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 15.4 MB (15359949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35eecb76c7d0d3257ad0d1322fa0f70fe5bb08f73cd35791e40dedfeb7df855e`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0e9b73e0ca3e835463c5e23f4651e5b72818127c694134646d41ab2c0f53cd`  
		Last Modified: Tue, 21 Nov 2023 13:01:50 GMT  
		Size: 424.2 MB (424161810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.6.3-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:f211f3e3a61b675d7224849c02f747fe37c022c469fd84188582509b3957b57c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **764.5 MB (764458663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e217b8b7e3451643249986f60289bcfa74c199c9f6079ce3cc42c1993a21099c`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:27 GMT
ADD file:ea38b381ee92d0c4b34697af5b78def83b881e6837b309e1f41a14bee2ff2b7e in / 
# Tue, 21 Nov 2023 06:27:27 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:00:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:00:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:01:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:18 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 08:21:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 08:21:25 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 08:21:28 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 08:25:34 GMT
ARG GHC=9.6.3
# Tue, 21 Nov 2023 08:25:34 GMT
ARG GHC_RELEASE_KEY=33C3A599DB85EA9B8BAA1866B202264020068BFB
# Tue, 21 Nov 2023 08:27:02 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.6.3 GHC_RELEASE_KEY=33C3A599DB85EA9B8BAA1866B202264020068BFB STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='03c389859319f09452081310fc13af7525063ea8930830ef76be2a14b312271e';             ;;         'x86_64')             GHC_SHA256='9ba0458c84efdbba69509c3c57497e22ad03743f816eb9c8b024abc13f7aacaa';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 08:27:15 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 08:27:15 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:357c576c57e480da5e7eb018506db51d822da9f357c02a76f7c4da1ccaa61b33`  
		Last Modified: Tue, 21 Nov 2023 06:31:24 GMT  
		Size: 49.3 MB (49291145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9750a1d4e9cc8d118fb8f247658f2e931026ab641d4ebdc3c3806b3dd8ee4d0d`  
		Last Modified: Tue, 21 Nov 2023 08:07:51 GMT  
		Size: 17.5 MB (17454097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55295586deeb07a4153f5f4d0cd2723a2240e52697d6ad85612c498057c0d832`  
		Last Modified: Tue, 21 Nov 2023 08:08:06 GMT  
		Size: 52.2 MB (52207152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fb9e461a1bbc28daea6d98c6425175d5ec238091b9c6d22306c3d257de50cd`  
		Last Modified: Tue, 21 Nov 2023 08:08:31 GMT  
		Size: 183.5 MB (183476090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8520593e4d4d8289c877a174b696c2830f14eb2b1b3a3a832ad50cb64aa23049`  
		Last Modified: Tue, 21 Nov 2023 08:39:07 GMT  
		Size: 517.3 KB (517300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234bbe5f5278dc328477465898a776d8addb6172cfc0ae55d199f015a74987c`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 17.2 MB (17230042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ed20186e4d0efa5eec675e66c421203c5fe383a529511ab58816cb659b96a0`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 12.4 MB (12373189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c393754494c424e8db0ad3483bff80207f1096cce794937df0bdfd2806d4ce`  
		Last Modified: Tue, 21 Nov 2023 08:42:50 GMT  
		Size: 431.9 MB (431909648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.6.3-slim`

```console
$ docker pull haskell@sha256:6a2ca8fe3d7ff3a9ace0dce72ac5c7ad562106e5a2b77bdc22ade682143cabf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.6.3-slim` - linux; amd64

```console
$ docker pull haskell@sha256:bb2f4fac9fd4ccbaf0b127b22aab26bafe00a78827d6ffa8a2847f7993b33bdc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.4 MB (427375116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4743189a29af3ade5951af6bc7d987310a85227b5edb930112160bb7867a507c`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:20 GMT
ADD file:7672eb709be933bb0edec47b8141cd2ebff266a770dfae1278205f7cee43c71a in / 
# Tue, 21 Nov 2023 05:22:20 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:41:56 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:42:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:42:21 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:42:24 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:46:13 GMT
ARG GHC=9.6.3
# Tue, 21 Nov 2023 12:46:13 GMT
ARG GHC_RELEASE_KEY=33C3A599DB85EA9B8BAA1866B202264020068BFB
# Tue, 21 Nov 2023 12:47:44 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.6.3 GHC_RELEASE_KEY=33C3A599DB85EA9B8BAA1866B202264020068BFB STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='03c389859319f09452081310fc13af7525063ea8930830ef76be2a14b312271e';             ;;         'x86_64')             GHC_SHA256='9ba0458c84efdbba69509c3c57497e22ad03743f816eb9c8b024abc13f7aacaa';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:47:50 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:47:50 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0fc9206bc4affb32fe13185a20b8184271c753e9b7cb81484bf770054fc69737`  
		Last Modified: Tue, 21 Nov 2023 05:27:19 GMT  
		Size: 27.2 MB (27187457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6213b4299e71dcc2c16c339ec043da12cc47384caa53a9f15259996652e6bf4`  
		Last Modified: Tue, 21 Nov 2023 12:59:36 GMT  
		Size: 94.0 MB (94045021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19344eacbd857e0b61cb66092db6d11c467aed149978f45a1dcdb057ebb9980`  
		Last Modified: Tue, 21 Nov 2023 12:59:24 GMT  
		Size: 15.4 MB (15359960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefb56630c3948901bac3dd75868f7d017f4b46579498b8fdf054347f3db9894`  
		Last Modified: Tue, 21 Nov 2023 12:59:23 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb31202f8acd4cff09dcb1643dbd5a4b9b62bf6563fe92ad9c416e8ff6d8d24a`  
		Last Modified: Tue, 21 Nov 2023 13:02:54 GMT  
		Size: 282.9 MB (282944310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.6.3-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:04b2c704eab0b9b5213a7cee276c5a151781707f137dff25d49273d938da03d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.7 MB (433696151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27101b331a316e834c75644567b15ff81696dd19dfa2ecec2f9250fcb1a56fff`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:39 GMT
ADD file:f60673c303a98b4e4c676e3403bc1b7cb316335aba1202205188176810494c07 in / 
# Tue, 19 Dec 2023 01:41:40 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:46:03 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 02:46:21 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK=2.11.1
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 19 Dec 2023 02:46:31 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 19 Dec 2023 02:46:34 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 19 Dec 2023 02:48:28 GMT
ARG GHC=9.6.3
# Tue, 19 Dec 2023 02:48:28 GMT
ARG GHC_RELEASE_KEY=33C3A599DB85EA9B8BAA1866B202264020068BFB
# Tue, 19 Dec 2023 02:49:48 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.6.3 GHC_RELEASE_KEY=33C3A599DB85EA9B8BAA1866B202264020068BFB STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='03c389859319f09452081310fc13af7525063ea8930830ef76be2a14b312271e';             ;;         'x86_64')             GHC_SHA256='9ba0458c84efdbba69509c3c57497e22ad03743f816eb9c8b024abc13f7aacaa';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 19 Dec 2023 02:49:58 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 02:49:58 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c0b0171eefd1c6d7f85c54d4a609269c9b5e19a0fd8cd787a49c808c6b73cf74`  
		Last Modified: Tue, 19 Dec 2023 01:46:01 GMT  
		Size: 26.0 MB (25969827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6ed82599775f9bbd4cc3c5df2ebf7342daaa490b970568c1ea375e3242ebc4`  
		Last Modified: Tue, 19 Dec 2023 02:55:11 GMT  
		Size: 88.1 MB (88053431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a99edfe152899f2001989c0e6103ad6f2276cf961df3dbb4aceefec5312d373`  
		Last Modified: Tue, 19 Dec 2023 02:55:02 GMT  
		Size: 17.2 MB (17230056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20252565f8094ddee6562ad5f30ebc81e720ba92b526c0174372c3fad25e8625`  
		Last Modified: Tue, 19 Dec 2023 02:55:01 GMT  
		Size: 12.4 MB (12373194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0df18857542919d351ed6263e743602c25e62587c8a679a4945c41fb77665af`  
		Last Modified: Tue, 19 Dec 2023 02:56:48 GMT  
		Size: 290.1 MB (290069643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.6.3-slim-buster`

```console
$ docker pull haskell@sha256:6a2ca8fe3d7ff3a9ace0dce72ac5c7ad562106e5a2b77bdc22ade682143cabf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.6.3-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:bb2f4fac9fd4ccbaf0b127b22aab26bafe00a78827d6ffa8a2847f7993b33bdc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.4 MB (427375116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4743189a29af3ade5951af6bc7d987310a85227b5edb930112160bb7867a507c`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:20 GMT
ADD file:7672eb709be933bb0edec47b8141cd2ebff266a770dfae1278205f7cee43c71a in / 
# Tue, 21 Nov 2023 05:22:20 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:41:56 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:42:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:42:21 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:42:24 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:46:13 GMT
ARG GHC=9.6.3
# Tue, 21 Nov 2023 12:46:13 GMT
ARG GHC_RELEASE_KEY=33C3A599DB85EA9B8BAA1866B202264020068BFB
# Tue, 21 Nov 2023 12:47:44 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.6.3 GHC_RELEASE_KEY=33C3A599DB85EA9B8BAA1866B202264020068BFB STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='03c389859319f09452081310fc13af7525063ea8930830ef76be2a14b312271e';             ;;         'x86_64')             GHC_SHA256='9ba0458c84efdbba69509c3c57497e22ad03743f816eb9c8b024abc13f7aacaa';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:47:50 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:47:50 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0fc9206bc4affb32fe13185a20b8184271c753e9b7cb81484bf770054fc69737`  
		Last Modified: Tue, 21 Nov 2023 05:27:19 GMT  
		Size: 27.2 MB (27187457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6213b4299e71dcc2c16c339ec043da12cc47384caa53a9f15259996652e6bf4`  
		Last Modified: Tue, 21 Nov 2023 12:59:36 GMT  
		Size: 94.0 MB (94045021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19344eacbd857e0b61cb66092db6d11c467aed149978f45a1dcdb057ebb9980`  
		Last Modified: Tue, 21 Nov 2023 12:59:24 GMT  
		Size: 15.4 MB (15359960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefb56630c3948901bac3dd75868f7d017f4b46579498b8fdf054347f3db9894`  
		Last Modified: Tue, 21 Nov 2023 12:59:23 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb31202f8acd4cff09dcb1643dbd5a4b9b62bf6563fe92ad9c416e8ff6d8d24a`  
		Last Modified: Tue, 21 Nov 2023 13:02:54 GMT  
		Size: 282.9 MB (282944310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.6.3-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:04b2c704eab0b9b5213a7cee276c5a151781707f137dff25d49273d938da03d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.7 MB (433696151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27101b331a316e834c75644567b15ff81696dd19dfa2ecec2f9250fcb1a56fff`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:39 GMT
ADD file:f60673c303a98b4e4c676e3403bc1b7cb316335aba1202205188176810494c07 in / 
# Tue, 19 Dec 2023 01:41:40 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:46:03 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 02:46:21 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK=2.11.1
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 19 Dec 2023 02:46:31 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 19 Dec 2023 02:46:34 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 19 Dec 2023 02:48:28 GMT
ARG GHC=9.6.3
# Tue, 19 Dec 2023 02:48:28 GMT
ARG GHC_RELEASE_KEY=33C3A599DB85EA9B8BAA1866B202264020068BFB
# Tue, 19 Dec 2023 02:49:48 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.6.3 GHC_RELEASE_KEY=33C3A599DB85EA9B8BAA1866B202264020068BFB STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='03c389859319f09452081310fc13af7525063ea8930830ef76be2a14b312271e';             ;;         'x86_64')             GHC_SHA256='9ba0458c84efdbba69509c3c57497e22ad03743f816eb9c8b024abc13f7aacaa';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 19 Dec 2023 02:49:58 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 02:49:58 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c0b0171eefd1c6d7f85c54d4a609269c9b5e19a0fd8cd787a49c808c6b73cf74`  
		Last Modified: Tue, 19 Dec 2023 01:46:01 GMT  
		Size: 26.0 MB (25969827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6ed82599775f9bbd4cc3c5df2ebf7342daaa490b970568c1ea375e3242ebc4`  
		Last Modified: Tue, 19 Dec 2023 02:55:11 GMT  
		Size: 88.1 MB (88053431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a99edfe152899f2001989c0e6103ad6f2276cf961df3dbb4aceefec5312d373`  
		Last Modified: Tue, 19 Dec 2023 02:55:02 GMT  
		Size: 17.2 MB (17230056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20252565f8094ddee6562ad5f30ebc81e720ba92b526c0174372c3fad25e8625`  
		Last Modified: Tue, 19 Dec 2023 02:55:01 GMT  
		Size: 12.4 MB (12373194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0df18857542919d351ed6263e743602c25e62587c8a679a4945c41fb77665af`  
		Last Modified: Tue, 19 Dec 2023 02:56:48 GMT  
		Size: 290.1 MB (290069643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.8`

```console
$ docker pull haskell@sha256:0d951e083ab7089d8de9ec0e5eb142eaefd70ec6b1de7d5da8a38d16afec38f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.8` - linux; amd64

```console
$ docker pull haskell@sha256:4980ba75628c7718b4c9b6745f4f89f8ddd9f34dca6c99e44e68d78f126c23e8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.4 MB (776377925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b5ce25e74c90a93b499beec7d97268d61bc3f9de57eb375165b09043fdbd9a`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:08 GMT
ADD file:4f8b7a35280160ec5a55323fa07ac91e294c86e2ea647ba212053983ef380bcf in / 
# Tue, 21 Nov 2023 05:22:08 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:55:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:56:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:57:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:47 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:39:51 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:39:55 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:39:58 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:39:58 GMT
ARG GHC=9.8.1
# Tue, 21 Nov 2023 12:39:58 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 21 Nov 2023 12:41:39 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.8.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='aab7af72614f8bf9ca624407aa4dbc69bc009c2b4cc1a0f3c062008db81bdb95';             ;;         'x86_64')             GHC_SHA256='d498657ca00514bc4620b591f74b93f9a3b64e5282e5c4e2876a734c130f1fbf';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:41:46 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:41:46 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b32028968d56a86ac35eac062e7abba276c547ab175fb057973c469eb41db55b`  
		Last Modified: Tue, 21 Nov 2023 05:26:57 GMT  
		Size: 50.5 MB (50499471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24c059838ae87ccefc35d50177e4e280a9e6f2f54127456ad0eaa5be5ed5386`  
		Last Modified: Tue, 21 Nov 2023 10:03:28 GMT  
		Size: 17.6 MB (17583860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819458a39dea8d30616a22068e79bcb7743745aa8b0d35fdb762ba69d98e3ec0`  
		Last Modified: Tue, 21 Nov 2023 10:03:45 GMT  
		Size: 51.9 MB (51874180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedd23d9034d9de62653c3bb2a2ca71fb88a1c6d17f386c0bfe4ac5bf8163929`  
		Last Modified: Tue, 21 Nov 2023 10:04:21 GMT  
		Size: 191.9 MB (191910019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ef9a56930d28877c2fa90904a7be44f1f8cca3356383b7f74682c75d8d994`  
		Last Modified: Tue, 21 Nov 2023 12:57:42 GMT  
		Size: 515.2 KB (515154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a1f56bfe415e8ae3055b472ce7df60a5bdf1033339c4dd235e31d400eb34c3`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 15.4 MB (15359949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35eecb76c7d0d3257ad0d1322fa0f70fe5bb08f73cd35791e40dedfeb7df855e`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8af2da252abb99a9c81a472596ee087886baad4962118fe1d876c34e7411515`  
		Last Modified: Tue, 21 Nov 2023 12:58:59 GMT  
		Size: 440.8 MB (440796924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.8` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:fbcca4aa25ce81d1ab6394e57ee65731ac1db80da098f4bbb596c2dea45e5535
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **781.9 MB (781863866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eeee2b51045fdea358f3b07474255e2fde2ecbb95984cec270e3b99fc72e262`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:27 GMT
ADD file:ea38b381ee92d0c4b34697af5b78def83b881e6837b309e1f41a14bee2ff2b7e in / 
# Tue, 21 Nov 2023 06:27:27 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:00:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:00:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:01:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:18 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 08:21:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 08:21:25 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 08:21:28 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 08:21:28 GMT
ARG GHC=9.8.1
# Tue, 21 Nov 2023 08:21:28 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 21 Nov 2023 08:23:06 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.8.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='aab7af72614f8bf9ca624407aa4dbc69bc009c2b4cc1a0f3c062008db81bdb95';             ;;         'x86_64')             GHC_SHA256='d498657ca00514bc4620b591f74b93f9a3b64e5282e5c4e2876a734c130f1fbf';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 08:23:18 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 08:23:19 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:357c576c57e480da5e7eb018506db51d822da9f357c02a76f7c4da1ccaa61b33`  
		Last Modified: Tue, 21 Nov 2023 06:31:24 GMT  
		Size: 49.3 MB (49291145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9750a1d4e9cc8d118fb8f247658f2e931026ab641d4ebdc3c3806b3dd8ee4d0d`  
		Last Modified: Tue, 21 Nov 2023 08:07:51 GMT  
		Size: 17.5 MB (17454097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55295586deeb07a4153f5f4d0cd2723a2240e52697d6ad85612c498057c0d832`  
		Last Modified: Tue, 21 Nov 2023 08:08:06 GMT  
		Size: 52.2 MB (52207152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fb9e461a1bbc28daea6d98c6425175d5ec238091b9c6d22306c3d257de50cd`  
		Last Modified: Tue, 21 Nov 2023 08:08:31 GMT  
		Size: 183.5 MB (183476090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8520593e4d4d8289c877a174b696c2830f14eb2b1b3a3a832ad50cb64aa23049`  
		Last Modified: Tue, 21 Nov 2023 08:39:07 GMT  
		Size: 517.3 KB (517300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234bbe5f5278dc328477465898a776d8addb6172cfc0ae55d199f015a74987c`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 17.2 MB (17230042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ed20186e4d0efa5eec675e66c421203c5fe383a529511ab58816cb659b96a0`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 12.4 MB (12373189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43422b7863f897378a29540b4f90bb753c6f1bf0e4988c233e62989f587e6ad8`  
		Last Modified: Tue, 21 Nov 2023 08:40:14 GMT  
		Size: 449.3 MB (449314851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.8-buster`

```console
$ docker pull haskell@sha256:0d951e083ab7089d8de9ec0e5eb142eaefd70ec6b1de7d5da8a38d16afec38f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.8-buster` - linux; amd64

```console
$ docker pull haskell@sha256:4980ba75628c7718b4c9b6745f4f89f8ddd9f34dca6c99e44e68d78f126c23e8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.4 MB (776377925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b5ce25e74c90a93b499beec7d97268d61bc3f9de57eb375165b09043fdbd9a`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:08 GMT
ADD file:4f8b7a35280160ec5a55323fa07ac91e294c86e2ea647ba212053983ef380bcf in / 
# Tue, 21 Nov 2023 05:22:08 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:55:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:56:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:57:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:47 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:39:51 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:39:55 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:39:58 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:39:58 GMT
ARG GHC=9.8.1
# Tue, 21 Nov 2023 12:39:58 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 21 Nov 2023 12:41:39 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.8.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='aab7af72614f8bf9ca624407aa4dbc69bc009c2b4cc1a0f3c062008db81bdb95';             ;;         'x86_64')             GHC_SHA256='d498657ca00514bc4620b591f74b93f9a3b64e5282e5c4e2876a734c130f1fbf';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:41:46 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:41:46 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b32028968d56a86ac35eac062e7abba276c547ab175fb057973c469eb41db55b`  
		Last Modified: Tue, 21 Nov 2023 05:26:57 GMT  
		Size: 50.5 MB (50499471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24c059838ae87ccefc35d50177e4e280a9e6f2f54127456ad0eaa5be5ed5386`  
		Last Modified: Tue, 21 Nov 2023 10:03:28 GMT  
		Size: 17.6 MB (17583860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819458a39dea8d30616a22068e79bcb7743745aa8b0d35fdb762ba69d98e3ec0`  
		Last Modified: Tue, 21 Nov 2023 10:03:45 GMT  
		Size: 51.9 MB (51874180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedd23d9034d9de62653c3bb2a2ca71fb88a1c6d17f386c0bfe4ac5bf8163929`  
		Last Modified: Tue, 21 Nov 2023 10:04:21 GMT  
		Size: 191.9 MB (191910019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ef9a56930d28877c2fa90904a7be44f1f8cca3356383b7f74682c75d8d994`  
		Last Modified: Tue, 21 Nov 2023 12:57:42 GMT  
		Size: 515.2 KB (515154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a1f56bfe415e8ae3055b472ce7df60a5bdf1033339c4dd235e31d400eb34c3`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 15.4 MB (15359949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35eecb76c7d0d3257ad0d1322fa0f70fe5bb08f73cd35791e40dedfeb7df855e`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8af2da252abb99a9c81a472596ee087886baad4962118fe1d876c34e7411515`  
		Last Modified: Tue, 21 Nov 2023 12:58:59 GMT  
		Size: 440.8 MB (440796924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.8-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:fbcca4aa25ce81d1ab6394e57ee65731ac1db80da098f4bbb596c2dea45e5535
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **781.9 MB (781863866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eeee2b51045fdea358f3b07474255e2fde2ecbb95984cec270e3b99fc72e262`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:27 GMT
ADD file:ea38b381ee92d0c4b34697af5b78def83b881e6837b309e1f41a14bee2ff2b7e in / 
# Tue, 21 Nov 2023 06:27:27 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:00:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:00:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:01:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:18 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 08:21:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 08:21:25 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 08:21:28 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 08:21:28 GMT
ARG GHC=9.8.1
# Tue, 21 Nov 2023 08:21:28 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 21 Nov 2023 08:23:06 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.8.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='aab7af72614f8bf9ca624407aa4dbc69bc009c2b4cc1a0f3c062008db81bdb95';             ;;         'x86_64')             GHC_SHA256='d498657ca00514bc4620b591f74b93f9a3b64e5282e5c4e2876a734c130f1fbf';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 08:23:18 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 08:23:19 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:357c576c57e480da5e7eb018506db51d822da9f357c02a76f7c4da1ccaa61b33`  
		Last Modified: Tue, 21 Nov 2023 06:31:24 GMT  
		Size: 49.3 MB (49291145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9750a1d4e9cc8d118fb8f247658f2e931026ab641d4ebdc3c3806b3dd8ee4d0d`  
		Last Modified: Tue, 21 Nov 2023 08:07:51 GMT  
		Size: 17.5 MB (17454097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55295586deeb07a4153f5f4d0cd2723a2240e52697d6ad85612c498057c0d832`  
		Last Modified: Tue, 21 Nov 2023 08:08:06 GMT  
		Size: 52.2 MB (52207152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fb9e461a1bbc28daea6d98c6425175d5ec238091b9c6d22306c3d257de50cd`  
		Last Modified: Tue, 21 Nov 2023 08:08:31 GMT  
		Size: 183.5 MB (183476090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8520593e4d4d8289c877a174b696c2830f14eb2b1b3a3a832ad50cb64aa23049`  
		Last Modified: Tue, 21 Nov 2023 08:39:07 GMT  
		Size: 517.3 KB (517300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234bbe5f5278dc328477465898a776d8addb6172cfc0ae55d199f015a74987c`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 17.2 MB (17230042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ed20186e4d0efa5eec675e66c421203c5fe383a529511ab58816cb659b96a0`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 12.4 MB (12373189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43422b7863f897378a29540b4f90bb753c6f1bf0e4988c233e62989f587e6ad8`  
		Last Modified: Tue, 21 Nov 2023 08:40:14 GMT  
		Size: 449.3 MB (449314851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.8-slim`

```console
$ docker pull haskell@sha256:29baea3db36c4a985f95bb1a4530d43073278ea4103a10a5dc968254d94b235d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.8-slim` - linux; amd64

```console
$ docker pull haskell@sha256:858b76cb891a02f4ced5fd2c2626cc26fd6a6f1054f2dcc05647729a214a50b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.6 MB (440611509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82237bb5b6bc25c2590d0feecb0b38ddc2420c9a9dbf5449f3b99cc3e357e3f2`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:20 GMT
ADD file:7672eb709be933bb0edec47b8141cd2ebff266a770dfae1278205f7cee43c71a in / 
# Tue, 21 Nov 2023 05:22:20 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:41:56 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:42:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:42:21 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:42:24 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:42:24 GMT
ARG GHC=9.8.1
# Tue, 21 Nov 2023 12:42:24 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 21 Nov 2023 12:43:59 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.8.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='aab7af72614f8bf9ca624407aa4dbc69bc009c2b4cc1a0f3c062008db81bdb95';             ;;         'x86_64')             GHC_SHA256='d498657ca00514bc4620b591f74b93f9a3b64e5282e5c4e2876a734c130f1fbf';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:44:05 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:44:05 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0fc9206bc4affb32fe13185a20b8184271c753e9b7cb81484bf770054fc69737`  
		Last Modified: Tue, 21 Nov 2023 05:27:19 GMT  
		Size: 27.2 MB (27187457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6213b4299e71dcc2c16c339ec043da12cc47384caa53a9f15259996652e6bf4`  
		Last Modified: Tue, 21 Nov 2023 12:59:36 GMT  
		Size: 94.0 MB (94045021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19344eacbd857e0b61cb66092db6d11c467aed149978f45a1dcdb057ebb9980`  
		Last Modified: Tue, 21 Nov 2023 12:59:24 GMT  
		Size: 15.4 MB (15359960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefb56630c3948901bac3dd75868f7d017f4b46579498b8fdf054347f3db9894`  
		Last Modified: Tue, 21 Nov 2023 12:59:23 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691c29c1b65c9a94e88a29baf35e37dc0dc3f7e5e2228ad58480cced1a0de925`  
		Last Modified: Tue, 21 Nov 2023 13:00:14 GMT  
		Size: 296.2 MB (296180703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.8-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:8fb474264853e6be6007319bf8e2bd44475878d391bfaa4a5514db11f7b9c9cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.5 MB (447484012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe30b2fc483028ca9f909ab40fd8c7add1905982844b35d0ff95e3c274fad370`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:39 GMT
ADD file:f60673c303a98b4e4c676e3403bc1b7cb316335aba1202205188176810494c07 in / 
# Tue, 19 Dec 2023 01:41:40 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:46:03 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 02:46:21 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK=2.11.1
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 19 Dec 2023 02:46:31 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 19 Dec 2023 02:46:34 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 19 Dec 2023 02:46:34 GMT
ARG GHC=9.8.1
# Tue, 19 Dec 2023 02:46:34 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 19 Dec 2023 02:48:05 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.8.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='aab7af72614f8bf9ca624407aa4dbc69bc009c2b4cc1a0f3c062008db81bdb95';             ;;         'x86_64')             GHC_SHA256='d498657ca00514bc4620b591f74b93f9a3b64e5282e5c4e2876a734c130f1fbf';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 19 Dec 2023 02:48:16 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 02:48:17 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c0b0171eefd1c6d7f85c54d4a609269c9b5e19a0fd8cd787a49c808c6b73cf74`  
		Last Modified: Tue, 19 Dec 2023 01:46:01 GMT  
		Size: 26.0 MB (25969827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6ed82599775f9bbd4cc3c5df2ebf7342daaa490b970568c1ea375e3242ebc4`  
		Last Modified: Tue, 19 Dec 2023 02:55:11 GMT  
		Size: 88.1 MB (88053431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a99edfe152899f2001989c0e6103ad6f2276cf961df3dbb4aceefec5312d373`  
		Last Modified: Tue, 19 Dec 2023 02:55:02 GMT  
		Size: 17.2 MB (17230056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20252565f8094ddee6562ad5f30ebc81e720ba92b526c0174372c3fad25e8625`  
		Last Modified: Tue, 19 Dec 2023 02:55:01 GMT  
		Size: 12.4 MB (12373194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df373a3b6f590305ac40bf712eb84f342145370ea6225181d41b1fe3229f6178`  
		Last Modified: Tue, 19 Dec 2023 02:55:44 GMT  
		Size: 303.9 MB (303857504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.8-slim-buster`

```console
$ docker pull haskell@sha256:29baea3db36c4a985f95bb1a4530d43073278ea4103a10a5dc968254d94b235d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.8-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:858b76cb891a02f4ced5fd2c2626cc26fd6a6f1054f2dcc05647729a214a50b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.6 MB (440611509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82237bb5b6bc25c2590d0feecb0b38ddc2420c9a9dbf5449f3b99cc3e357e3f2`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:20 GMT
ADD file:7672eb709be933bb0edec47b8141cd2ebff266a770dfae1278205f7cee43c71a in / 
# Tue, 21 Nov 2023 05:22:20 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:41:56 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:42:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:42:21 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:42:24 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:42:24 GMT
ARG GHC=9.8.1
# Tue, 21 Nov 2023 12:42:24 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 21 Nov 2023 12:43:59 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.8.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='aab7af72614f8bf9ca624407aa4dbc69bc009c2b4cc1a0f3c062008db81bdb95';             ;;         'x86_64')             GHC_SHA256='d498657ca00514bc4620b591f74b93f9a3b64e5282e5c4e2876a734c130f1fbf';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:44:05 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:44:05 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0fc9206bc4affb32fe13185a20b8184271c753e9b7cb81484bf770054fc69737`  
		Last Modified: Tue, 21 Nov 2023 05:27:19 GMT  
		Size: 27.2 MB (27187457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6213b4299e71dcc2c16c339ec043da12cc47384caa53a9f15259996652e6bf4`  
		Last Modified: Tue, 21 Nov 2023 12:59:36 GMT  
		Size: 94.0 MB (94045021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19344eacbd857e0b61cb66092db6d11c467aed149978f45a1dcdb057ebb9980`  
		Last Modified: Tue, 21 Nov 2023 12:59:24 GMT  
		Size: 15.4 MB (15359960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefb56630c3948901bac3dd75868f7d017f4b46579498b8fdf054347f3db9894`  
		Last Modified: Tue, 21 Nov 2023 12:59:23 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691c29c1b65c9a94e88a29baf35e37dc0dc3f7e5e2228ad58480cced1a0de925`  
		Last Modified: Tue, 21 Nov 2023 13:00:14 GMT  
		Size: 296.2 MB (296180703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.8-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:8fb474264853e6be6007319bf8e2bd44475878d391bfaa4a5514db11f7b9c9cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.5 MB (447484012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe30b2fc483028ca9f909ab40fd8c7add1905982844b35d0ff95e3c274fad370`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:39 GMT
ADD file:f60673c303a98b4e4c676e3403bc1b7cb316335aba1202205188176810494c07 in / 
# Tue, 19 Dec 2023 01:41:40 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:46:03 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 02:46:21 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK=2.11.1
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 19 Dec 2023 02:46:31 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 19 Dec 2023 02:46:34 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 19 Dec 2023 02:46:34 GMT
ARG GHC=9.8.1
# Tue, 19 Dec 2023 02:46:34 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 19 Dec 2023 02:48:05 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.8.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='aab7af72614f8bf9ca624407aa4dbc69bc009c2b4cc1a0f3c062008db81bdb95';             ;;         'x86_64')             GHC_SHA256='d498657ca00514bc4620b591f74b93f9a3b64e5282e5c4e2876a734c130f1fbf';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 19 Dec 2023 02:48:16 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 02:48:17 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c0b0171eefd1c6d7f85c54d4a609269c9b5e19a0fd8cd787a49c808c6b73cf74`  
		Last Modified: Tue, 19 Dec 2023 01:46:01 GMT  
		Size: 26.0 MB (25969827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6ed82599775f9bbd4cc3c5df2ebf7342daaa490b970568c1ea375e3242ebc4`  
		Last Modified: Tue, 19 Dec 2023 02:55:11 GMT  
		Size: 88.1 MB (88053431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a99edfe152899f2001989c0e6103ad6f2276cf961df3dbb4aceefec5312d373`  
		Last Modified: Tue, 19 Dec 2023 02:55:02 GMT  
		Size: 17.2 MB (17230056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20252565f8094ddee6562ad5f30ebc81e720ba92b526c0174372c3fad25e8625`  
		Last Modified: Tue, 19 Dec 2023 02:55:01 GMT  
		Size: 12.4 MB (12373194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df373a3b6f590305ac40bf712eb84f342145370ea6225181d41b1fe3229f6178`  
		Last Modified: Tue, 19 Dec 2023 02:55:44 GMT  
		Size: 303.9 MB (303857504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.8.1`

```console
$ docker pull haskell@sha256:0d951e083ab7089d8de9ec0e5eb142eaefd70ec6b1de7d5da8a38d16afec38f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.8.1` - linux; amd64

```console
$ docker pull haskell@sha256:4980ba75628c7718b4c9b6745f4f89f8ddd9f34dca6c99e44e68d78f126c23e8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.4 MB (776377925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b5ce25e74c90a93b499beec7d97268d61bc3f9de57eb375165b09043fdbd9a`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:08 GMT
ADD file:4f8b7a35280160ec5a55323fa07ac91e294c86e2ea647ba212053983ef380bcf in / 
# Tue, 21 Nov 2023 05:22:08 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:55:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:56:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:57:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:47 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:39:51 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:39:55 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:39:58 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:39:58 GMT
ARG GHC=9.8.1
# Tue, 21 Nov 2023 12:39:58 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 21 Nov 2023 12:41:39 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.8.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='aab7af72614f8bf9ca624407aa4dbc69bc009c2b4cc1a0f3c062008db81bdb95';             ;;         'x86_64')             GHC_SHA256='d498657ca00514bc4620b591f74b93f9a3b64e5282e5c4e2876a734c130f1fbf';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:41:46 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:41:46 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b32028968d56a86ac35eac062e7abba276c547ab175fb057973c469eb41db55b`  
		Last Modified: Tue, 21 Nov 2023 05:26:57 GMT  
		Size: 50.5 MB (50499471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24c059838ae87ccefc35d50177e4e280a9e6f2f54127456ad0eaa5be5ed5386`  
		Last Modified: Tue, 21 Nov 2023 10:03:28 GMT  
		Size: 17.6 MB (17583860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819458a39dea8d30616a22068e79bcb7743745aa8b0d35fdb762ba69d98e3ec0`  
		Last Modified: Tue, 21 Nov 2023 10:03:45 GMT  
		Size: 51.9 MB (51874180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedd23d9034d9de62653c3bb2a2ca71fb88a1c6d17f386c0bfe4ac5bf8163929`  
		Last Modified: Tue, 21 Nov 2023 10:04:21 GMT  
		Size: 191.9 MB (191910019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ef9a56930d28877c2fa90904a7be44f1f8cca3356383b7f74682c75d8d994`  
		Last Modified: Tue, 21 Nov 2023 12:57:42 GMT  
		Size: 515.2 KB (515154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a1f56bfe415e8ae3055b472ce7df60a5bdf1033339c4dd235e31d400eb34c3`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 15.4 MB (15359949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35eecb76c7d0d3257ad0d1322fa0f70fe5bb08f73cd35791e40dedfeb7df855e`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8af2da252abb99a9c81a472596ee087886baad4962118fe1d876c34e7411515`  
		Last Modified: Tue, 21 Nov 2023 12:58:59 GMT  
		Size: 440.8 MB (440796924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.8.1` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:fbcca4aa25ce81d1ab6394e57ee65731ac1db80da098f4bbb596c2dea45e5535
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **781.9 MB (781863866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eeee2b51045fdea358f3b07474255e2fde2ecbb95984cec270e3b99fc72e262`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:27 GMT
ADD file:ea38b381ee92d0c4b34697af5b78def83b881e6837b309e1f41a14bee2ff2b7e in / 
# Tue, 21 Nov 2023 06:27:27 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:00:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:00:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:01:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:18 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 08:21:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 08:21:25 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 08:21:28 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 08:21:28 GMT
ARG GHC=9.8.1
# Tue, 21 Nov 2023 08:21:28 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 21 Nov 2023 08:23:06 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.8.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='aab7af72614f8bf9ca624407aa4dbc69bc009c2b4cc1a0f3c062008db81bdb95';             ;;         'x86_64')             GHC_SHA256='d498657ca00514bc4620b591f74b93f9a3b64e5282e5c4e2876a734c130f1fbf';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 08:23:18 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 08:23:19 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:357c576c57e480da5e7eb018506db51d822da9f357c02a76f7c4da1ccaa61b33`  
		Last Modified: Tue, 21 Nov 2023 06:31:24 GMT  
		Size: 49.3 MB (49291145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9750a1d4e9cc8d118fb8f247658f2e931026ab641d4ebdc3c3806b3dd8ee4d0d`  
		Last Modified: Tue, 21 Nov 2023 08:07:51 GMT  
		Size: 17.5 MB (17454097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55295586deeb07a4153f5f4d0cd2723a2240e52697d6ad85612c498057c0d832`  
		Last Modified: Tue, 21 Nov 2023 08:08:06 GMT  
		Size: 52.2 MB (52207152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fb9e461a1bbc28daea6d98c6425175d5ec238091b9c6d22306c3d257de50cd`  
		Last Modified: Tue, 21 Nov 2023 08:08:31 GMT  
		Size: 183.5 MB (183476090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8520593e4d4d8289c877a174b696c2830f14eb2b1b3a3a832ad50cb64aa23049`  
		Last Modified: Tue, 21 Nov 2023 08:39:07 GMT  
		Size: 517.3 KB (517300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234bbe5f5278dc328477465898a776d8addb6172cfc0ae55d199f015a74987c`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 17.2 MB (17230042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ed20186e4d0efa5eec675e66c421203c5fe383a529511ab58816cb659b96a0`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 12.4 MB (12373189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43422b7863f897378a29540b4f90bb753c6f1bf0e4988c233e62989f587e6ad8`  
		Last Modified: Tue, 21 Nov 2023 08:40:14 GMT  
		Size: 449.3 MB (449314851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.8.1-buster`

```console
$ docker pull haskell@sha256:0d951e083ab7089d8de9ec0e5eb142eaefd70ec6b1de7d5da8a38d16afec38f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.8.1-buster` - linux; amd64

```console
$ docker pull haskell@sha256:4980ba75628c7718b4c9b6745f4f89f8ddd9f34dca6c99e44e68d78f126c23e8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.4 MB (776377925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b5ce25e74c90a93b499beec7d97268d61bc3f9de57eb375165b09043fdbd9a`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:08 GMT
ADD file:4f8b7a35280160ec5a55323fa07ac91e294c86e2ea647ba212053983ef380bcf in / 
# Tue, 21 Nov 2023 05:22:08 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:55:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:56:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:57:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:47 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:39:51 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:39:55 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:39:58 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:39:58 GMT
ARG GHC=9.8.1
# Tue, 21 Nov 2023 12:39:58 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 21 Nov 2023 12:41:39 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.8.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='aab7af72614f8bf9ca624407aa4dbc69bc009c2b4cc1a0f3c062008db81bdb95';             ;;         'x86_64')             GHC_SHA256='d498657ca00514bc4620b591f74b93f9a3b64e5282e5c4e2876a734c130f1fbf';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:41:46 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:41:46 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b32028968d56a86ac35eac062e7abba276c547ab175fb057973c469eb41db55b`  
		Last Modified: Tue, 21 Nov 2023 05:26:57 GMT  
		Size: 50.5 MB (50499471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24c059838ae87ccefc35d50177e4e280a9e6f2f54127456ad0eaa5be5ed5386`  
		Last Modified: Tue, 21 Nov 2023 10:03:28 GMT  
		Size: 17.6 MB (17583860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819458a39dea8d30616a22068e79bcb7743745aa8b0d35fdb762ba69d98e3ec0`  
		Last Modified: Tue, 21 Nov 2023 10:03:45 GMT  
		Size: 51.9 MB (51874180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedd23d9034d9de62653c3bb2a2ca71fb88a1c6d17f386c0bfe4ac5bf8163929`  
		Last Modified: Tue, 21 Nov 2023 10:04:21 GMT  
		Size: 191.9 MB (191910019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ef9a56930d28877c2fa90904a7be44f1f8cca3356383b7f74682c75d8d994`  
		Last Modified: Tue, 21 Nov 2023 12:57:42 GMT  
		Size: 515.2 KB (515154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a1f56bfe415e8ae3055b472ce7df60a5bdf1033339c4dd235e31d400eb34c3`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 15.4 MB (15359949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35eecb76c7d0d3257ad0d1322fa0f70fe5bb08f73cd35791e40dedfeb7df855e`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8af2da252abb99a9c81a472596ee087886baad4962118fe1d876c34e7411515`  
		Last Modified: Tue, 21 Nov 2023 12:58:59 GMT  
		Size: 440.8 MB (440796924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.8.1-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:fbcca4aa25ce81d1ab6394e57ee65731ac1db80da098f4bbb596c2dea45e5535
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **781.9 MB (781863866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eeee2b51045fdea358f3b07474255e2fde2ecbb95984cec270e3b99fc72e262`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:27 GMT
ADD file:ea38b381ee92d0c4b34697af5b78def83b881e6837b309e1f41a14bee2ff2b7e in / 
# Tue, 21 Nov 2023 06:27:27 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:00:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:00:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:01:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:18 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 08:21:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 08:21:25 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 08:21:28 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 08:21:28 GMT
ARG GHC=9.8.1
# Tue, 21 Nov 2023 08:21:28 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 21 Nov 2023 08:23:06 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.8.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='aab7af72614f8bf9ca624407aa4dbc69bc009c2b4cc1a0f3c062008db81bdb95';             ;;         'x86_64')             GHC_SHA256='d498657ca00514bc4620b591f74b93f9a3b64e5282e5c4e2876a734c130f1fbf';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 08:23:18 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 08:23:19 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:357c576c57e480da5e7eb018506db51d822da9f357c02a76f7c4da1ccaa61b33`  
		Last Modified: Tue, 21 Nov 2023 06:31:24 GMT  
		Size: 49.3 MB (49291145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9750a1d4e9cc8d118fb8f247658f2e931026ab641d4ebdc3c3806b3dd8ee4d0d`  
		Last Modified: Tue, 21 Nov 2023 08:07:51 GMT  
		Size: 17.5 MB (17454097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55295586deeb07a4153f5f4d0cd2723a2240e52697d6ad85612c498057c0d832`  
		Last Modified: Tue, 21 Nov 2023 08:08:06 GMT  
		Size: 52.2 MB (52207152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fb9e461a1bbc28daea6d98c6425175d5ec238091b9c6d22306c3d257de50cd`  
		Last Modified: Tue, 21 Nov 2023 08:08:31 GMT  
		Size: 183.5 MB (183476090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8520593e4d4d8289c877a174b696c2830f14eb2b1b3a3a832ad50cb64aa23049`  
		Last Modified: Tue, 21 Nov 2023 08:39:07 GMT  
		Size: 517.3 KB (517300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234bbe5f5278dc328477465898a776d8addb6172cfc0ae55d199f015a74987c`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 17.2 MB (17230042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ed20186e4d0efa5eec675e66c421203c5fe383a529511ab58816cb659b96a0`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 12.4 MB (12373189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43422b7863f897378a29540b4f90bb753c6f1bf0e4988c233e62989f587e6ad8`  
		Last Modified: Tue, 21 Nov 2023 08:40:14 GMT  
		Size: 449.3 MB (449314851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.8.1-slim`

```console
$ docker pull haskell@sha256:29baea3db36c4a985f95bb1a4530d43073278ea4103a10a5dc968254d94b235d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.8.1-slim` - linux; amd64

```console
$ docker pull haskell@sha256:858b76cb891a02f4ced5fd2c2626cc26fd6a6f1054f2dcc05647729a214a50b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.6 MB (440611509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82237bb5b6bc25c2590d0feecb0b38ddc2420c9a9dbf5449f3b99cc3e357e3f2`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:20 GMT
ADD file:7672eb709be933bb0edec47b8141cd2ebff266a770dfae1278205f7cee43c71a in / 
# Tue, 21 Nov 2023 05:22:20 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:41:56 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:42:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:42:21 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:42:24 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:42:24 GMT
ARG GHC=9.8.1
# Tue, 21 Nov 2023 12:42:24 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 21 Nov 2023 12:43:59 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.8.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='aab7af72614f8bf9ca624407aa4dbc69bc009c2b4cc1a0f3c062008db81bdb95';             ;;         'x86_64')             GHC_SHA256='d498657ca00514bc4620b591f74b93f9a3b64e5282e5c4e2876a734c130f1fbf';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:44:05 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:44:05 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0fc9206bc4affb32fe13185a20b8184271c753e9b7cb81484bf770054fc69737`  
		Last Modified: Tue, 21 Nov 2023 05:27:19 GMT  
		Size: 27.2 MB (27187457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6213b4299e71dcc2c16c339ec043da12cc47384caa53a9f15259996652e6bf4`  
		Last Modified: Tue, 21 Nov 2023 12:59:36 GMT  
		Size: 94.0 MB (94045021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19344eacbd857e0b61cb66092db6d11c467aed149978f45a1dcdb057ebb9980`  
		Last Modified: Tue, 21 Nov 2023 12:59:24 GMT  
		Size: 15.4 MB (15359960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefb56630c3948901bac3dd75868f7d017f4b46579498b8fdf054347f3db9894`  
		Last Modified: Tue, 21 Nov 2023 12:59:23 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691c29c1b65c9a94e88a29baf35e37dc0dc3f7e5e2228ad58480cced1a0de925`  
		Last Modified: Tue, 21 Nov 2023 13:00:14 GMT  
		Size: 296.2 MB (296180703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.8.1-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:8fb474264853e6be6007319bf8e2bd44475878d391bfaa4a5514db11f7b9c9cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.5 MB (447484012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe30b2fc483028ca9f909ab40fd8c7add1905982844b35d0ff95e3c274fad370`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:39 GMT
ADD file:f60673c303a98b4e4c676e3403bc1b7cb316335aba1202205188176810494c07 in / 
# Tue, 19 Dec 2023 01:41:40 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:46:03 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 02:46:21 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK=2.11.1
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 19 Dec 2023 02:46:31 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 19 Dec 2023 02:46:34 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 19 Dec 2023 02:46:34 GMT
ARG GHC=9.8.1
# Tue, 19 Dec 2023 02:46:34 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 19 Dec 2023 02:48:05 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.8.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='aab7af72614f8bf9ca624407aa4dbc69bc009c2b4cc1a0f3c062008db81bdb95';             ;;         'x86_64')             GHC_SHA256='d498657ca00514bc4620b591f74b93f9a3b64e5282e5c4e2876a734c130f1fbf';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 19 Dec 2023 02:48:16 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 02:48:17 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c0b0171eefd1c6d7f85c54d4a609269c9b5e19a0fd8cd787a49c808c6b73cf74`  
		Last Modified: Tue, 19 Dec 2023 01:46:01 GMT  
		Size: 26.0 MB (25969827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6ed82599775f9bbd4cc3c5df2ebf7342daaa490b970568c1ea375e3242ebc4`  
		Last Modified: Tue, 19 Dec 2023 02:55:11 GMT  
		Size: 88.1 MB (88053431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a99edfe152899f2001989c0e6103ad6f2276cf961df3dbb4aceefec5312d373`  
		Last Modified: Tue, 19 Dec 2023 02:55:02 GMT  
		Size: 17.2 MB (17230056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20252565f8094ddee6562ad5f30ebc81e720ba92b526c0174372c3fad25e8625`  
		Last Modified: Tue, 19 Dec 2023 02:55:01 GMT  
		Size: 12.4 MB (12373194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df373a3b6f590305ac40bf712eb84f342145370ea6225181d41b1fe3229f6178`  
		Last Modified: Tue, 19 Dec 2023 02:55:44 GMT  
		Size: 303.9 MB (303857504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.8.1-slim-buster`

```console
$ docker pull haskell@sha256:29baea3db36c4a985f95bb1a4530d43073278ea4103a10a5dc968254d94b235d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.8.1-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:858b76cb891a02f4ced5fd2c2626cc26fd6a6f1054f2dcc05647729a214a50b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.6 MB (440611509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82237bb5b6bc25c2590d0feecb0b38ddc2420c9a9dbf5449f3b99cc3e357e3f2`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:20 GMT
ADD file:7672eb709be933bb0edec47b8141cd2ebff266a770dfae1278205f7cee43c71a in / 
# Tue, 21 Nov 2023 05:22:20 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:41:56 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:42:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:42:21 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:42:24 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:42:24 GMT
ARG GHC=9.8.1
# Tue, 21 Nov 2023 12:42:24 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 21 Nov 2023 12:43:59 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.8.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='aab7af72614f8bf9ca624407aa4dbc69bc009c2b4cc1a0f3c062008db81bdb95';             ;;         'x86_64')             GHC_SHA256='d498657ca00514bc4620b591f74b93f9a3b64e5282e5c4e2876a734c130f1fbf';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:44:05 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:44:05 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0fc9206bc4affb32fe13185a20b8184271c753e9b7cb81484bf770054fc69737`  
		Last Modified: Tue, 21 Nov 2023 05:27:19 GMT  
		Size: 27.2 MB (27187457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6213b4299e71dcc2c16c339ec043da12cc47384caa53a9f15259996652e6bf4`  
		Last Modified: Tue, 21 Nov 2023 12:59:36 GMT  
		Size: 94.0 MB (94045021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19344eacbd857e0b61cb66092db6d11c467aed149978f45a1dcdb057ebb9980`  
		Last Modified: Tue, 21 Nov 2023 12:59:24 GMT  
		Size: 15.4 MB (15359960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefb56630c3948901bac3dd75868f7d017f4b46579498b8fdf054347f3db9894`  
		Last Modified: Tue, 21 Nov 2023 12:59:23 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691c29c1b65c9a94e88a29baf35e37dc0dc3f7e5e2228ad58480cced1a0de925`  
		Last Modified: Tue, 21 Nov 2023 13:00:14 GMT  
		Size: 296.2 MB (296180703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.8.1-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:8fb474264853e6be6007319bf8e2bd44475878d391bfaa4a5514db11f7b9c9cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.5 MB (447484012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe30b2fc483028ca9f909ab40fd8c7add1905982844b35d0ff95e3c274fad370`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:39 GMT
ADD file:f60673c303a98b4e4c676e3403bc1b7cb316335aba1202205188176810494c07 in / 
# Tue, 19 Dec 2023 01:41:40 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:46:03 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 02:46:21 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK=2.11.1
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 19 Dec 2023 02:46:31 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 19 Dec 2023 02:46:34 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 19 Dec 2023 02:46:34 GMT
ARG GHC=9.8.1
# Tue, 19 Dec 2023 02:46:34 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 19 Dec 2023 02:48:05 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.8.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='aab7af72614f8bf9ca624407aa4dbc69bc009c2b4cc1a0f3c062008db81bdb95';             ;;         'x86_64')             GHC_SHA256='d498657ca00514bc4620b591f74b93f9a3b64e5282e5c4e2876a734c130f1fbf';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 19 Dec 2023 02:48:16 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 02:48:17 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c0b0171eefd1c6d7f85c54d4a609269c9b5e19a0fd8cd787a49c808c6b73cf74`  
		Last Modified: Tue, 19 Dec 2023 01:46:01 GMT  
		Size: 26.0 MB (25969827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6ed82599775f9bbd4cc3c5df2ebf7342daaa490b970568c1ea375e3242ebc4`  
		Last Modified: Tue, 19 Dec 2023 02:55:11 GMT  
		Size: 88.1 MB (88053431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a99edfe152899f2001989c0e6103ad6f2276cf961df3dbb4aceefec5312d373`  
		Last Modified: Tue, 19 Dec 2023 02:55:02 GMT  
		Size: 17.2 MB (17230056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20252565f8094ddee6562ad5f30ebc81e720ba92b526c0174372c3fad25e8625`  
		Last Modified: Tue, 19 Dec 2023 02:55:01 GMT  
		Size: 12.4 MB (12373194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df373a3b6f590305ac40bf712eb84f342145370ea6225181d41b1fe3229f6178`  
		Last Modified: Tue, 19 Dec 2023 02:55:44 GMT  
		Size: 303.9 MB (303857504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:buster`

```console
$ docker pull haskell@sha256:0d951e083ab7089d8de9ec0e5eb142eaefd70ec6b1de7d5da8a38d16afec38f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:buster` - linux; amd64

```console
$ docker pull haskell@sha256:4980ba75628c7718b4c9b6745f4f89f8ddd9f34dca6c99e44e68d78f126c23e8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.4 MB (776377925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b5ce25e74c90a93b499beec7d97268d61bc3f9de57eb375165b09043fdbd9a`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:08 GMT
ADD file:4f8b7a35280160ec5a55323fa07ac91e294c86e2ea647ba212053983ef380bcf in / 
# Tue, 21 Nov 2023 05:22:08 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:55:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:56:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:57:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:47 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:39:51 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:39:55 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:39:58 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:39:58 GMT
ARG GHC=9.8.1
# Tue, 21 Nov 2023 12:39:58 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 21 Nov 2023 12:41:39 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.8.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='aab7af72614f8bf9ca624407aa4dbc69bc009c2b4cc1a0f3c062008db81bdb95';             ;;         'x86_64')             GHC_SHA256='d498657ca00514bc4620b591f74b93f9a3b64e5282e5c4e2876a734c130f1fbf';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:41:46 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:41:46 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b32028968d56a86ac35eac062e7abba276c547ab175fb057973c469eb41db55b`  
		Last Modified: Tue, 21 Nov 2023 05:26:57 GMT  
		Size: 50.5 MB (50499471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24c059838ae87ccefc35d50177e4e280a9e6f2f54127456ad0eaa5be5ed5386`  
		Last Modified: Tue, 21 Nov 2023 10:03:28 GMT  
		Size: 17.6 MB (17583860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819458a39dea8d30616a22068e79bcb7743745aa8b0d35fdb762ba69d98e3ec0`  
		Last Modified: Tue, 21 Nov 2023 10:03:45 GMT  
		Size: 51.9 MB (51874180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedd23d9034d9de62653c3bb2a2ca71fb88a1c6d17f386c0bfe4ac5bf8163929`  
		Last Modified: Tue, 21 Nov 2023 10:04:21 GMT  
		Size: 191.9 MB (191910019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ef9a56930d28877c2fa90904a7be44f1f8cca3356383b7f74682c75d8d994`  
		Last Modified: Tue, 21 Nov 2023 12:57:42 GMT  
		Size: 515.2 KB (515154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a1f56bfe415e8ae3055b472ce7df60a5bdf1033339c4dd235e31d400eb34c3`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 15.4 MB (15359949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35eecb76c7d0d3257ad0d1322fa0f70fe5bb08f73cd35791e40dedfeb7df855e`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8af2da252abb99a9c81a472596ee087886baad4962118fe1d876c34e7411515`  
		Last Modified: Tue, 21 Nov 2023 12:58:59 GMT  
		Size: 440.8 MB (440796924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:fbcca4aa25ce81d1ab6394e57ee65731ac1db80da098f4bbb596c2dea45e5535
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **781.9 MB (781863866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eeee2b51045fdea358f3b07474255e2fde2ecbb95984cec270e3b99fc72e262`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:27 GMT
ADD file:ea38b381ee92d0c4b34697af5b78def83b881e6837b309e1f41a14bee2ff2b7e in / 
# Tue, 21 Nov 2023 06:27:27 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:00:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:00:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:01:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:18 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 08:21:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 08:21:25 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 08:21:28 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 08:21:28 GMT
ARG GHC=9.8.1
# Tue, 21 Nov 2023 08:21:28 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 21 Nov 2023 08:23:06 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.8.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='aab7af72614f8bf9ca624407aa4dbc69bc009c2b4cc1a0f3c062008db81bdb95';             ;;         'x86_64')             GHC_SHA256='d498657ca00514bc4620b591f74b93f9a3b64e5282e5c4e2876a734c130f1fbf';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 08:23:18 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 08:23:19 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:357c576c57e480da5e7eb018506db51d822da9f357c02a76f7c4da1ccaa61b33`  
		Last Modified: Tue, 21 Nov 2023 06:31:24 GMT  
		Size: 49.3 MB (49291145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9750a1d4e9cc8d118fb8f247658f2e931026ab641d4ebdc3c3806b3dd8ee4d0d`  
		Last Modified: Tue, 21 Nov 2023 08:07:51 GMT  
		Size: 17.5 MB (17454097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55295586deeb07a4153f5f4d0cd2723a2240e52697d6ad85612c498057c0d832`  
		Last Modified: Tue, 21 Nov 2023 08:08:06 GMT  
		Size: 52.2 MB (52207152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fb9e461a1bbc28daea6d98c6425175d5ec238091b9c6d22306c3d257de50cd`  
		Last Modified: Tue, 21 Nov 2023 08:08:31 GMT  
		Size: 183.5 MB (183476090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8520593e4d4d8289c877a174b696c2830f14eb2b1b3a3a832ad50cb64aa23049`  
		Last Modified: Tue, 21 Nov 2023 08:39:07 GMT  
		Size: 517.3 KB (517300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234bbe5f5278dc328477465898a776d8addb6172cfc0ae55d199f015a74987c`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 17.2 MB (17230042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ed20186e4d0efa5eec675e66c421203c5fe383a529511ab58816cb659b96a0`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 12.4 MB (12373189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43422b7863f897378a29540b4f90bb753c6f1bf0e4988c233e62989f587e6ad8`  
		Last Modified: Tue, 21 Nov 2023 08:40:14 GMT  
		Size: 449.3 MB (449314851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:latest`

```console
$ docker pull haskell@sha256:0d951e083ab7089d8de9ec0e5eb142eaefd70ec6b1de7d5da8a38d16afec38f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:latest` - linux; amd64

```console
$ docker pull haskell@sha256:4980ba75628c7718b4c9b6745f4f89f8ddd9f34dca6c99e44e68d78f126c23e8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.4 MB (776377925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b5ce25e74c90a93b499beec7d97268d61bc3f9de57eb375165b09043fdbd9a`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:08 GMT
ADD file:4f8b7a35280160ec5a55323fa07ac91e294c86e2ea647ba212053983ef380bcf in / 
# Tue, 21 Nov 2023 05:22:08 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 09:55:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:56:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 09:57:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:47 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:39:51 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:39:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:39:55 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:39:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:39:58 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:39:58 GMT
ARG GHC=9.8.1
# Tue, 21 Nov 2023 12:39:58 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 21 Nov 2023 12:41:39 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.8.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='aab7af72614f8bf9ca624407aa4dbc69bc009c2b4cc1a0f3c062008db81bdb95';             ;;         'x86_64')             GHC_SHA256='d498657ca00514bc4620b591f74b93f9a3b64e5282e5c4e2876a734c130f1fbf';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:41:46 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:41:46 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b32028968d56a86ac35eac062e7abba276c547ab175fb057973c469eb41db55b`  
		Last Modified: Tue, 21 Nov 2023 05:26:57 GMT  
		Size: 50.5 MB (50499471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24c059838ae87ccefc35d50177e4e280a9e6f2f54127456ad0eaa5be5ed5386`  
		Last Modified: Tue, 21 Nov 2023 10:03:28 GMT  
		Size: 17.6 MB (17583860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819458a39dea8d30616a22068e79bcb7743745aa8b0d35fdb762ba69d98e3ec0`  
		Last Modified: Tue, 21 Nov 2023 10:03:45 GMT  
		Size: 51.9 MB (51874180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedd23d9034d9de62653c3bb2a2ca71fb88a1c6d17f386c0bfe4ac5bf8163929`  
		Last Modified: Tue, 21 Nov 2023 10:04:21 GMT  
		Size: 191.9 MB (191910019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6ef9a56930d28877c2fa90904a7be44f1f8cca3356383b7f74682c75d8d994`  
		Last Modified: Tue, 21 Nov 2023 12:57:42 GMT  
		Size: 515.2 KB (515154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a1f56bfe415e8ae3055b472ce7df60a5bdf1033339c4dd235e31d400eb34c3`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 15.4 MB (15359949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35eecb76c7d0d3257ad0d1322fa0f70fe5bb08f73cd35791e40dedfeb7df855e`  
		Last Modified: Tue, 21 Nov 2023 12:57:44 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8af2da252abb99a9c81a472596ee087886baad4962118fe1d876c34e7411515`  
		Last Modified: Tue, 21 Nov 2023 12:58:59 GMT  
		Size: 440.8 MB (440796924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:latest` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:fbcca4aa25ce81d1ab6394e57ee65731ac1db80da098f4bbb596c2dea45e5535
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **781.9 MB (781863866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eeee2b51045fdea358f3b07474255e2fde2ecbb95984cec270e3b99fc72e262`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:27 GMT
ADD file:ea38b381ee92d0c4b34697af5b78def83b881e6837b309e1f41a14bee2ff2b7e in / 
# Tue, 21 Nov 2023 06:27:27 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 08:00:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:00:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:01:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:18 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 08:21:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 08:21:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 08:21:25 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 08:21:26 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 08:21:28 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 08:21:28 GMT
ARG GHC=9.8.1
# Tue, 21 Nov 2023 08:21:28 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 21 Nov 2023 08:23:06 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.8.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='aab7af72614f8bf9ca624407aa4dbc69bc009c2b4cc1a0f3c062008db81bdb95';             ;;         'x86_64')             GHC_SHA256='d498657ca00514bc4620b591f74b93f9a3b64e5282e5c4e2876a734c130f1fbf';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 08:23:18 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 08:23:19 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:357c576c57e480da5e7eb018506db51d822da9f357c02a76f7c4da1ccaa61b33`  
		Last Modified: Tue, 21 Nov 2023 06:31:24 GMT  
		Size: 49.3 MB (49291145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9750a1d4e9cc8d118fb8f247658f2e931026ab641d4ebdc3c3806b3dd8ee4d0d`  
		Last Modified: Tue, 21 Nov 2023 08:07:51 GMT  
		Size: 17.5 MB (17454097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55295586deeb07a4153f5f4d0cd2723a2240e52697d6ad85612c498057c0d832`  
		Last Modified: Tue, 21 Nov 2023 08:08:06 GMT  
		Size: 52.2 MB (52207152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fb9e461a1bbc28daea6d98c6425175d5ec238091b9c6d22306c3d257de50cd`  
		Last Modified: Tue, 21 Nov 2023 08:08:31 GMT  
		Size: 183.5 MB (183476090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8520593e4d4d8289c877a174b696c2830f14eb2b1b3a3a832ad50cb64aa23049`  
		Last Modified: Tue, 21 Nov 2023 08:39:07 GMT  
		Size: 517.3 KB (517300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234bbe5f5278dc328477465898a776d8addb6172cfc0ae55d199f015a74987c`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 17.2 MB (17230042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ed20186e4d0efa5eec675e66c421203c5fe383a529511ab58816cb659b96a0`  
		Last Modified: Tue, 21 Nov 2023 08:39:09 GMT  
		Size: 12.4 MB (12373189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43422b7863f897378a29540b4f90bb753c6f1bf0e4988c233e62989f587e6ad8`  
		Last Modified: Tue, 21 Nov 2023 08:40:14 GMT  
		Size: 449.3 MB (449314851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:slim`

```console
$ docker pull haskell@sha256:29baea3db36c4a985f95bb1a4530d43073278ea4103a10a5dc968254d94b235d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:slim` - linux; amd64

```console
$ docker pull haskell@sha256:858b76cb891a02f4ced5fd2c2626cc26fd6a6f1054f2dcc05647729a214a50b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.6 MB (440611509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82237bb5b6bc25c2590d0feecb0b38ddc2420c9a9dbf5449f3b99cc3e357e3f2`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:20 GMT
ADD file:7672eb709be933bb0edec47b8141cd2ebff266a770dfae1278205f7cee43c71a in / 
# Tue, 21 Nov 2023 05:22:20 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:41:56 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:42:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:42:21 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:42:24 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:42:24 GMT
ARG GHC=9.8.1
# Tue, 21 Nov 2023 12:42:24 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 21 Nov 2023 12:43:59 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.8.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='aab7af72614f8bf9ca624407aa4dbc69bc009c2b4cc1a0f3c062008db81bdb95';             ;;         'x86_64')             GHC_SHA256='d498657ca00514bc4620b591f74b93f9a3b64e5282e5c4e2876a734c130f1fbf';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:44:05 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:44:05 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0fc9206bc4affb32fe13185a20b8184271c753e9b7cb81484bf770054fc69737`  
		Last Modified: Tue, 21 Nov 2023 05:27:19 GMT  
		Size: 27.2 MB (27187457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6213b4299e71dcc2c16c339ec043da12cc47384caa53a9f15259996652e6bf4`  
		Last Modified: Tue, 21 Nov 2023 12:59:36 GMT  
		Size: 94.0 MB (94045021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19344eacbd857e0b61cb66092db6d11c467aed149978f45a1dcdb057ebb9980`  
		Last Modified: Tue, 21 Nov 2023 12:59:24 GMT  
		Size: 15.4 MB (15359960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefb56630c3948901bac3dd75868f7d017f4b46579498b8fdf054347f3db9894`  
		Last Modified: Tue, 21 Nov 2023 12:59:23 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691c29c1b65c9a94e88a29baf35e37dc0dc3f7e5e2228ad58480cced1a0de925`  
		Last Modified: Tue, 21 Nov 2023 13:00:14 GMT  
		Size: 296.2 MB (296180703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:8fb474264853e6be6007319bf8e2bd44475878d391bfaa4a5514db11f7b9c9cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.5 MB (447484012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe30b2fc483028ca9f909ab40fd8c7add1905982844b35d0ff95e3c274fad370`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:39 GMT
ADD file:f60673c303a98b4e4c676e3403bc1b7cb316335aba1202205188176810494c07 in / 
# Tue, 19 Dec 2023 01:41:40 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:46:03 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 02:46:21 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK=2.11.1
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 19 Dec 2023 02:46:31 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 19 Dec 2023 02:46:34 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 19 Dec 2023 02:46:34 GMT
ARG GHC=9.8.1
# Tue, 19 Dec 2023 02:46:34 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 19 Dec 2023 02:48:05 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.8.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='aab7af72614f8bf9ca624407aa4dbc69bc009c2b4cc1a0f3c062008db81bdb95';             ;;         'x86_64')             GHC_SHA256='d498657ca00514bc4620b591f74b93f9a3b64e5282e5c4e2876a734c130f1fbf';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 19 Dec 2023 02:48:16 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 02:48:17 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c0b0171eefd1c6d7f85c54d4a609269c9b5e19a0fd8cd787a49c808c6b73cf74`  
		Last Modified: Tue, 19 Dec 2023 01:46:01 GMT  
		Size: 26.0 MB (25969827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6ed82599775f9bbd4cc3c5df2ebf7342daaa490b970568c1ea375e3242ebc4`  
		Last Modified: Tue, 19 Dec 2023 02:55:11 GMT  
		Size: 88.1 MB (88053431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a99edfe152899f2001989c0e6103ad6f2276cf961df3dbb4aceefec5312d373`  
		Last Modified: Tue, 19 Dec 2023 02:55:02 GMT  
		Size: 17.2 MB (17230056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20252565f8094ddee6562ad5f30ebc81e720ba92b526c0174372c3fad25e8625`  
		Last Modified: Tue, 19 Dec 2023 02:55:01 GMT  
		Size: 12.4 MB (12373194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df373a3b6f590305ac40bf712eb84f342145370ea6225181d41b1fe3229f6178`  
		Last Modified: Tue, 19 Dec 2023 02:55:44 GMT  
		Size: 303.9 MB (303857504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:slim-buster`

```console
$ docker pull haskell@sha256:29baea3db36c4a985f95bb1a4530d43073278ea4103a10a5dc968254d94b235d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:858b76cb891a02f4ced5fd2c2626cc26fd6a6f1054f2dcc05647729a214a50b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.6 MB (440611509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82237bb5b6bc25c2590d0feecb0b38ddc2420c9a9dbf5449f3b99cc3e357e3f2`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 21 Nov 2023 05:22:20 GMT
ADD file:7672eb709be933bb0edec47b8141cd2ebff266a770dfae1278205f7cee43c71a in / 
# Tue, 21 Nov 2023 05:22:20 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:41:56 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 12:42:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK=2.11.1
# Tue, 21 Nov 2023 12:42:18 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 21 Nov 2023 12:42:21 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 21 Nov 2023 12:42:22 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 21 Nov 2023 12:42:24 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 21 Nov 2023 12:42:24 GMT
ARG GHC=9.8.1
# Tue, 21 Nov 2023 12:42:24 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 21 Nov 2023 12:43:59 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.8.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='aab7af72614f8bf9ca624407aa4dbc69bc009c2b4cc1a0f3c062008db81bdb95';             ;;         'x86_64')             GHC_SHA256='d498657ca00514bc4620b591f74b93f9a3b64e5282e5c4e2876a734c130f1fbf';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 21 Nov 2023 12:44:05 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 12:44:05 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0fc9206bc4affb32fe13185a20b8184271c753e9b7cb81484bf770054fc69737`  
		Last Modified: Tue, 21 Nov 2023 05:27:19 GMT  
		Size: 27.2 MB (27187457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6213b4299e71dcc2c16c339ec043da12cc47384caa53a9f15259996652e6bf4`  
		Last Modified: Tue, 21 Nov 2023 12:59:36 GMT  
		Size: 94.0 MB (94045021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19344eacbd857e0b61cb66092db6d11c467aed149978f45a1dcdb057ebb9980`  
		Last Modified: Tue, 21 Nov 2023 12:59:24 GMT  
		Size: 15.4 MB (15359960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefb56630c3948901bac3dd75868f7d017f4b46579498b8fdf054347f3db9894`  
		Last Modified: Tue, 21 Nov 2023 12:59:23 GMT  
		Size: 7.8 MB (7838368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691c29c1b65c9a94e88a29baf35e37dc0dc3f7e5e2228ad58480cced1a0de925`  
		Last Modified: Tue, 21 Nov 2023 13:00:14 GMT  
		Size: 296.2 MB (296180703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:8fb474264853e6be6007319bf8e2bd44475878d391bfaa4a5514db11f7b9c9cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.5 MB (447484012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe30b2fc483028ca9f909ab40fd8c7add1905982844b35d0ff95e3c274fad370`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:39 GMT
ADD file:f60673c303a98b4e4c676e3403bc1b7cb316335aba1202205188176810494c07 in / 
# Tue, 19 Dec 2023 01:41:40 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 02:46:03 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 02:46:21 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK=2.11.1
# Tue, 19 Dec 2023 02:46:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 19 Dec 2023 02:46:31 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL=3.8.1.0
# Tue, 19 Dec 2023 02:46:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Tue, 19 Dec 2023 02:46:34 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 19 Dec 2023 02:46:34 GMT
ARG GHC=9.8.1
# Tue, 19 Dec 2023 02:46:34 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 19 Dec 2023 02:48:05 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.8.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='aab7af72614f8bf9ca624407aa4dbc69bc009c2b4cc1a0f3c062008db81bdb95';             ;;         'x86_64')             GHC_SHA256='d498657ca00514bc4620b591f74b93f9a3b64e5282e5c4e2876a734c130f1fbf';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 19 Dec 2023 02:48:16 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 02:48:17 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c0b0171eefd1c6d7f85c54d4a609269c9b5e19a0fd8cd787a49c808c6b73cf74`  
		Last Modified: Tue, 19 Dec 2023 01:46:01 GMT  
		Size: 26.0 MB (25969827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6ed82599775f9bbd4cc3c5df2ebf7342daaa490b970568c1ea375e3242ebc4`  
		Last Modified: Tue, 19 Dec 2023 02:55:11 GMT  
		Size: 88.1 MB (88053431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a99edfe152899f2001989c0e6103ad6f2276cf961df3dbb4aceefec5312d373`  
		Last Modified: Tue, 19 Dec 2023 02:55:02 GMT  
		Size: 17.2 MB (17230056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20252565f8094ddee6562ad5f30ebc81e720ba92b526c0174372c3fad25e8625`  
		Last Modified: Tue, 19 Dec 2023 02:55:01 GMT  
		Size: 12.4 MB (12373194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df373a3b6f590305ac40bf712eb84f342145370ea6225181d41b1fe3229f6178`  
		Last Modified: Tue, 19 Dec 2023 02:55:44 GMT  
		Size: 303.9 MB (303857504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
