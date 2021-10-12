## `haskell:9-stretch`

```console
$ docker pull haskell@sha256:544ff4b67f165b4f76bffcee74c68700f996f11526658fd9b2bd22f7060a2d6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:9-stretch` - linux; amd64

```console
$ docker pull haskell@sha256:34c311ac7a66006825886b5bfcfb7b83302671ce6169c75949e2961a54461c70
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.1 MB (374101837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c00dbe8cea4a82a7f56b07977e0ab8f6a03d79d080751d9f67f94a20ae4045`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 12 Oct 2021 01:22:41 GMT
ADD file:084c8b3d38d578aa3910f3786b67b058962dbfdfd4a49d6e0201f2e91670873b in / 
# Tue, 12 Oct 2021 01:22:42 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 17:00:16 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 17:00:40 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 17:00:41 GMT
ARG CABAL_INSTALL=3.6.0.0
# Tue, 12 Oct 2021 17:00:41 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Tue, 12 Oct 2021 17:00:41 GMT
ARG CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
# Tue, 12 Oct 2021 17:00:50 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${CABAL_INSTALL_RELEASE_KEY} &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS.sig &&     gpg --batch --trusted-key B3D9F94B8DCAE210 --verify SHA256SUMS.sig SHA256SUMS &&     curl -fSL https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/cabal-install-$CABAL_INSTALL-x86_64-linux.tar.xz -o cabal-install.tar.gz &&     echo "$CABAL_INSTALL_RELEASE_SHA256 cabal-install.tar.gz" | sha256sum --strict --check &&     tar -xf cabal-install.tar.gz -C /usr/local/bin &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Tue, 12 Oct 2021 17:00:50 GMT
ARG GHC=9.0.1
# Tue, 12 Oct 2021 17:00:50 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 12 Oct 2021 17:00:50 GMT
ARG GHC_RELEASE_SHA256=4CA6252492F59FE589029FADCA4B6F922D6A9F0FF39D19A2BD9886FDE4E183D5
# Tue, 12 Oct 2021 17:01:59 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=9.0.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD GHC_RELEASE_SHA256=4CA6252492F59FE589029FADCA4B6F922D6A9F0FF39D19A2BD9886FDE4E183D5
RUN cd /tmp &&   export GNUPGHOME="$(mktemp -d)" &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb9-linux.tar.xz -o ghc.tar.xz &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb9-linux.tar.xz.sig -o ghc.tar.xz.sig &&   gpg --batch --keyserver keyserver.ubuntu.com --receive-keys ${GHC_RELEASE_KEY} &&   gpg --batch --trusted-key 2DE04D4E97DB64AD --verify ghc.tar.xz.sig ghc.tar.xz &&   echo "$GHC_RELEASE_SHA256 ghc.tar.xz" | sha256sum --strict --check &&   tar xf ghc.tar.xz &&   cd ghc-$GHC &&   ./configure --prefix /opt/ghc/$GHC &&   make install &&   find /opt/ghc/$GHC/ \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete &&   rm -rf /opt/ghc/$GHC/share/ &&   rm -rf "$GNUPGHOME" /tmp/*
# Tue, 12 Oct 2021 17:02:03 GMT
ARG STACK=2.7.3
# Tue, 12 Oct 2021 17:02:03 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 12 Oct 2021 17:02:03 GMT
ARG STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
# Tue, 12 Oct 2021 17:02:09 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=9.0.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD GHC_RELEASE_SHA256=4CA6252492F59FE589029FADCA4B6F922D6A9F0FF39D19A2BD9886FDE4E183D5 STACK=2.7.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     echo "$STACK_RELEASE_SHA256 stack.tar.gz" | sha256sum --strict --check &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 stack-$STACK-linux-x86_64/stack &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Tue, 12 Oct 2021 17:02:10 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 17:02:10 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:2f0ef4316716c8b8925ba3665932f8bf2cef3b072d82de1aeb269d6b8b61b84c`  
		Last Modified: Tue, 12 Oct 2021 01:29:27 GMT  
		Size: 45.4 MB (45379651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37ecbb4abc0889c2c8472ea1668a846a9645c6aac79ae1b9cb8f3963de371c6`  
		Last Modified: Tue, 12 Oct 2021 17:07:26 GMT  
		Size: 97.4 MB (97444892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:580f5908cc1a5a432c08d67d0a7e697395664ac9ede6e94ebb3e2fb8f04e5b36`  
		Last Modified: Tue, 12 Oct 2021 17:07:12 GMT  
		Size: 9.8 MB (9816054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e9a17d55ad3a8802e8274822ca8d340108f54183b01fcb122e6b439125fc80d`  
		Last Modified: Tue, 12 Oct 2021 17:07:55 GMT  
		Size: 203.6 MB (203559992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9302490dff99d31fe51a41f0057829934019416655bae3290a2555bfb133286`  
		Last Modified: Tue, 12 Oct 2021 17:07:13 GMT  
		Size: 17.9 MB (17901248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
