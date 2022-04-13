## `golang:1-stretch`

```console
$ docker pull golang@sha256:aa6cc59ff370d32a45dd4a6e369270b093c8463ae2927636eb903d4e5fc1e94f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `golang:1-stretch` - linux; amd64

```console
$ docker pull golang@sha256:22da03c1b275440c4df433945330ade13cc0f3e08bc2d87633fa71c298ee5c42
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310418135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bddfbb61ce4a6322485cbe80cca20a26989b3fd5ba617df6abd5e56d3616b17`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:24:03 GMT
ADD file:a2cdf89d4e169a3a32c563c96a92cd6ccac002820e53533c9a86fd8bf0fb5db8 in / 
# Tue, 29 Mar 2022 00:24:04 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:34:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:34:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 29 Mar 2022 17:34:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 22:09:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 22:09:57 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:20:13 GMT
ENV GOLANG_VERSION=1.18.1
# Wed, 13 Apr 2022 02:20:28 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18.1.linux-amd64.tar.gz'; 			sha256='b3b815f47ababac13810fc6021eb73d65478e0b2db4b09d348eefad9581a2334'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18.1.linux-armv6l.tar.gz'; 			sha256='9edc01c8e7db64e9ceeffc8258359e027812886ceca3444e83c4eb96ddb068ee'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18.1.linux-arm64.tar.gz'; 			sha256='56a91851c97fb4697077abbca38860f735c32b38993ff79b088dac46e4735633'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18.1.linux-386.tar.gz'; 			sha256='9a8df5dde9058f08ac01ecfaae42534610db398e487138788c01da26a0d41ff9'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18.1.linux-ppc64le.tar.gz'; 			sha256='33db623d1eecf362fe365107c12efc90eff0b9609e0b3345e258388019cb552a'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18.1.linux-s390x.tar.gz'; 			sha256='5d9301324148ed4dbfaa0800da43a843ffd65c834ee73fcf087255697c925f74'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 13 Apr 2022 02:20:29 GMT
ENV GOPATH=/go
# Wed, 13 Apr 2022 02:20:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:20:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 13 Apr 2022 02:20:30 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0030cc4ce25ce472fe488839def15ec8f2227bb916461b518cf534073c019a86`  
		Last Modified: Tue, 29 Mar 2022 00:30:44 GMT  
		Size: 45.4 MB (45427467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab54d469df647484a8ae344911382d9b4412045d3c0f6536e7442858952cc68`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 11.3 MB (11302267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c84a1692804545a237be30579f35e501652cab9a2d8babe2693e66e653c706f`  
		Last Modified: Tue, 29 Mar 2022 17:41:29 GMT  
		Size: 4.3 MB (4342926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628acdaf85032c817e9eb7f4749b887f3733c8c590d2e3c2f396f2051406557f`  
		Last Modified: Tue, 29 Mar 2022 17:41:47 GMT  
		Size: 49.8 MB (49765499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7687e96bf02e7b84e87c99c672a3ffb64edd6216b1c86d52da8987b36b5e48`  
		Last Modified: Wed, 30 Mar 2022 22:13:22 GMT  
		Size: 57.9 MB (57878724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f88eed85e40e853e9ac478f21de9bd135faae2323c4b9e6f16f6e697e4582d0`  
		Last Modified: Wed, 13 Apr 2022 02:30:09 GMT  
		Size: 141.7 MB (141701096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3ac9f9076e94303134cf4a5290517adec85d488aeab59c8a2e96c8973a2cbc`  
		Last Modified: Wed, 13 Apr 2022 02:29:47 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-stretch` - linux; arm variant v7

```console
$ docker pull golang@sha256:4833c2e062ac70fbec1d9a3632b85442ee372ee92ebf71cb45005c9cc61e47e8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258382467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79fc5e8a97650ee2a0b914b3234dd4aecd849a3f53f336f9ad5bc286b3de0081`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 02:23:57 GMT
ADD file:3dc1697adfcf63a288e9ec7a2c40438b8ba2ccfff0382a1ed5457f30d7a37f76 in / 
# Tue, 29 Mar 2022 02:23:57 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 20:17:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 20:17:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 20:18:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 31 Mar 2022 23:31:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 31 Mar 2022 23:31:53 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 04:15:58 GMT
ENV GOLANG_VERSION=1.18.1
# Wed, 13 Apr 2022 04:16:32 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18.1.linux-amd64.tar.gz'; 			sha256='b3b815f47ababac13810fc6021eb73d65478e0b2db4b09d348eefad9581a2334'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18.1.linux-armv6l.tar.gz'; 			sha256='9edc01c8e7db64e9ceeffc8258359e027812886ceca3444e83c4eb96ddb068ee'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18.1.linux-arm64.tar.gz'; 			sha256='56a91851c97fb4697077abbca38860f735c32b38993ff79b088dac46e4735633'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18.1.linux-386.tar.gz'; 			sha256='9a8df5dde9058f08ac01ecfaae42534610db398e487138788c01da26a0d41ff9'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18.1.linux-ppc64le.tar.gz'; 			sha256='33db623d1eecf362fe365107c12efc90eff0b9609e0b3345e258388019cb552a'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18.1.linux-s390x.tar.gz'; 			sha256='5d9301324148ed4dbfaa0800da43a843ffd65c834ee73fcf087255697c925f74'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 13 Apr 2022 04:16:34 GMT
ENV GOPATH=/go
# Wed, 13 Apr 2022 04:16:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 04:16:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 13 Apr 2022 04:16:36 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:aecfa9e0b0179abf68bebbcfc35453928546e01ad1c8b6eaadf759360762dada`  
		Last Modified: Tue, 29 Mar 2022 02:40:33 GMT  
		Size: 42.2 MB (42151158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11bc36fcf6b269b843685f3e40183609c9ee393c766145d636666727cc97069e`  
		Last Modified: Wed, 30 Mar 2022 21:38:43 GMT  
		Size: 10.0 MB (9956889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e13cc08b3e8cd7b26260c7597b624d4a45ebc2afb89bb5da193fc824ab69e55`  
		Last Modified: Wed, 30 Mar 2022 21:38:39 GMT  
		Size: 3.9 MB (3921802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842f17f357dbe1ebb8ad0508d83e0bcbf9dd99dd8dc3a9084a153a6c61aec7fe`  
		Last Modified: Wed, 30 Mar 2022 21:39:26 GMT  
		Size: 46.1 MB (46128132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af016c133cc1b7459f7c0e45c2dff45e5a108efe7d973bd7c078a85b2343414`  
		Last Modified: Thu, 31 Mar 2022 23:42:13 GMT  
		Size: 46.2 MB (46206717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd4bb6e899438f71b551e5b870514cb2cc3d42411df4af98d7c61777f4088e5`  
		Last Modified: Wed, 13 Apr 2022 04:41:09 GMT  
		Size: 110.0 MB (110017614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07261c98a8c23d83c65139db951b6bb4361236998a77a1c72325b9f75227ee30`  
		Last Modified: Wed, 13 Apr 2022 04:39:54 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-stretch` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:978863414c9009d3ec60fd59900a5e5966196afff67ad6cb9f334e415f4a8c6b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.8 MB (262779699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b3cd0b1e4eb899d1e2947ff12f4f5fb30f10ab849acc7d47c4209270eb22fd1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:45:21 GMT
ADD file:cfa91852b5b893603b656848cb1329c06041fea5cfef841978456c7266e6ac11 in / 
# Tue, 29 Mar 2022 00:45:22 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:18:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 02:18:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 02:18:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 22:46:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 22:46:21 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:40:39 GMT
ENV GOLANG_VERSION=1.18.1
# Wed, 13 Apr 2022 02:40:52 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18.1.linux-amd64.tar.gz'; 			sha256='b3b815f47ababac13810fc6021eb73d65478e0b2db4b09d348eefad9581a2334'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18.1.linux-armv6l.tar.gz'; 			sha256='9edc01c8e7db64e9ceeffc8258359e027812886ceca3444e83c4eb96ddb068ee'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18.1.linux-arm64.tar.gz'; 			sha256='56a91851c97fb4697077abbca38860f735c32b38993ff79b088dac46e4735633'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18.1.linux-386.tar.gz'; 			sha256='9a8df5dde9058f08ac01ecfaae42534610db398e487138788c01da26a0d41ff9'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18.1.linux-ppc64le.tar.gz'; 			sha256='33db623d1eecf362fe365107c12efc90eff0b9609e0b3345e258388019cb552a'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18.1.linux-s390x.tar.gz'; 			sha256='5d9301324148ed4dbfaa0800da43a843ffd65c834ee73fcf087255697c925f74'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 13 Apr 2022 02:40:54 GMT
ENV GOPATH=/go
# Wed, 13 Apr 2022 02:40:55 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:40:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 13 Apr 2022 02:40:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0b62b1ed6f218f82ac797884bd7a8c5dcdcdd8d003f3946678c53900cc537d7b`  
		Last Modified: Tue, 29 Mar 2022 00:53:52 GMT  
		Size: 43.2 MB (43212837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e309f576f536ef1eb431f346fb1a09b23c355e6ec7657db9b1b5d59d58c839`  
		Last Modified: Wed, 30 Mar 2022 02:27:51 GMT  
		Size: 10.2 MB (10217976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91984a52400cf1b768b1f46910222bcf8cb584650c23a648535dab2f65b3ef9`  
		Last Modified: Wed, 30 Mar 2022 02:27:51 GMT  
		Size: 3.9 MB (3874485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30bf42292398504e3d3c25878dc1c8db3cfee75868876d30db31722bf5880fe8`  
		Last Modified: Wed, 30 Mar 2022 02:28:10 GMT  
		Size: 47.7 MB (47736638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f3e613da9f3743fc7ba0eed8136a3815e3c64fef74b9ced113be2da23b9901`  
		Last Modified: Wed, 30 Mar 2022 22:50:41 GMT  
		Size: 49.0 MB (49039344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91426448b225bc917f9be6982c8b4c7fa0f655a194aa8b66128fca828c4b9d3e`  
		Last Modified: Wed, 13 Apr 2022 02:51:05 GMT  
		Size: 108.7 MB (108698293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3b14b1760ce642dbc36294a9d2932a5122791f3a1477a38ee829383b8e540e`  
		Last Modified: Wed, 13 Apr 2022 02:50:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-stretch` - linux; 386

```console
$ docker pull golang@sha256:026ec6dd7264404fed8b0fb5391b91b9180dbc786ce87f99f0ca05425268687b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.1 MB (288141903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4e3bab8a5fa3884475f438a7dcdf6df5d3a85990e8771b63a4edc9cc90add82`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:44:09 GMT
ADD file:74aa6d4005ba30e0fb6af0b75158bccd03c55e837be6f73f1c2929f62028a19d in / 
# Tue, 29 Mar 2022 00:44:10 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 18:02:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 18:02:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 29 Mar 2022 18:02:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 00:54:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 00:54:40 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:39:29 GMT
ENV GOLANG_VERSION=1.18.1
# Wed, 13 Apr 2022 02:39:43 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18.1.linux-amd64.tar.gz'; 			sha256='b3b815f47ababac13810fc6021eb73d65478e0b2db4b09d348eefad9581a2334'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18.1.linux-armv6l.tar.gz'; 			sha256='9edc01c8e7db64e9ceeffc8258359e027812886ceca3444e83c4eb96ddb068ee'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18.1.linux-arm64.tar.gz'; 			sha256='56a91851c97fb4697077abbca38860f735c32b38993ff79b088dac46e4735633'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18.1.linux-386.tar.gz'; 			sha256='9a8df5dde9058f08ac01ecfaae42534610db398e487138788c01da26a0d41ff9'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18.1.linux-ppc64le.tar.gz'; 			sha256='33db623d1eecf362fe365107c12efc90eff0b9609e0b3345e258388019cb552a'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18.1.linux-s390x.tar.gz'; 			sha256='5d9301324148ed4dbfaa0800da43a843ffd65c834ee73fcf087255697c925f74'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 13 Apr 2022 02:39:44 GMT
ENV GOPATH=/go
# Wed, 13 Apr 2022 02:39:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:39:47 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 13 Apr 2022 02:39:48 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d8b8952dbc41a74d8004d044b352e7f612041bf00ab66401180cd3af79d35a14`  
		Last Modified: Tue, 29 Mar 2022 00:53:10 GMT  
		Size: 46.1 MB (46147573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:434a4f3f3baec793c431715991d82fb56bfbd9cf0a0bbf4279af77c453529ee8`  
		Last Modified: Tue, 29 Mar 2022 18:18:40 GMT  
		Size: 11.4 MB (11358228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f9948fe9b0550578499ca71c9ec007e18340e37504109404d1b54634960324`  
		Last Modified: Tue, 29 Mar 2022 18:18:39 GMT  
		Size: 4.3 MB (4342256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fe7fe28ce5da9cf227db9f102ead8076b04ec82e230f682c42a1fdfc441795`  
		Last Modified: Tue, 29 Mar 2022 18:18:59 GMT  
		Size: 51.3 MB (51267629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f381c6d48db608d55408ae5e77fd7dc02378f10c8e2c1aea7b7050d2dbe00db4`  
		Last Modified: Wed, 30 Mar 2022 00:59:25 GMT  
		Size: 62.2 MB (62170155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0597d22d01f5bc112ef585a200f11d65943b0dc8c98ff5c57e3a4e9f065f016d`  
		Last Modified: Wed, 13 Apr 2022 02:51:23 GMT  
		Size: 112.9 MB (112855936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7014e8ad221c8bde3b642876bbf99e94f242e4198178d0f5b15f059020a69a0`  
		Last Modified: Wed, 13 Apr 2022 02:51:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
