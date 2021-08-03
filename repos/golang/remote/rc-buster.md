## `golang:rc-buster`

```console
$ docker pull golang@sha256:6a76592e19556facf9cb7a5da08ffafd573dc7e90646105ff8501e6fe3059af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `golang:rc-buster` - linux; amd64

```console
$ docker pull golang@sha256:e25407049eb26b9ff749afca5b069ee246f89c3f343c455053a16356a9b01adb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.6 MB (323641972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:794146d0b0d406c68fd107123a853f9e1d3d37a0e5181314f686e7e6b0ab43e6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:30 GMT
ADD file:e952f6979e4b0ead00b6906db1dd70eb9beb564a04e2f02e2e0cff8614920216 in / 
# Thu, 22 Jul 2021 00:45:31 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 01:12:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:12:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 01:12:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 02:01:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 02:01:18 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jul 2021 02:01:19 GMT
ENV GOLANG_VERSION=1.17rc1
# Fri, 23 Jul 2021 02:01:37 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.17rc1.linux-amd64.tar.gz'; 			sha256='bfbd3881a01ca3826777b1c40f241acacd45b14730d373259cd673d74e15e534'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17rc1.linux-armv6l.tar.gz'; 			sha256='1fd5c3733d6fab5ebcb3ca6ae2b478d370bb0638ba3966284ed7e7aa97acfc8a'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17rc1.linux-arm64.tar.gz'; 			sha256='7498e426ce814a94a1d271d6bb80b9a2cf8c77ec49df531c57bd7a9ff82cfa4e'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17rc1.linux-386.tar.gz'; 			sha256='e9b78a4bd98165b86bb887643f58cc0464cc7ff7fae12516fc43114809c71e07'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17rc1.linux-ppc64le.tar.gz'; 			sha256='d3aec884d6cbb8504bb25591a780759dd0ea5d9ede2a5e6af1dfe210df0a60f1'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17rc1.linux-s390x.tar.gz'; 			sha256='23318ad51bd3d164aed307b500b9e89174e7df425a0cd03e619b65bbd65d6b19'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17rc1.src.tar.gz'; 		sha256='0d63be0f3abc79d35efcb60dfce4445e64bb1ea194edcfd9783a76316b7e85e2'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 23 Jul 2021 02:01:39 GMT
ENV GOPATH=/go
# Fri, 23 Jul 2021 02:01:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jul 2021 02:01:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 23 Jul 2021 02:01:40 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:627b765e08d177e63c9a202ca4991b711448905b934435c70b7cbd7d4a9c7959`  
		Last Modified: Thu, 22 Jul 2021 00:50:07 GMT  
		Size: 50.4 MB (50435626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c040670e5e559fd936db175530ad4c1dd014bd25b2bf25ea19fa20554fe2d736`  
		Last Modified: Thu, 22 Jul 2021 01:19:54 GMT  
		Size: 7.8 MB (7832944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073a180f4992853fa3dd8da604e7b041bc8ea92157749d042c0853312f178f6a`  
		Last Modified: Thu, 22 Jul 2021 01:19:54 GMT  
		Size: 10.0 MB (9997222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf76209566d0c8d78df205b09e6e5b52ff7f10cb4e1c03d9336ed7dd2decd919`  
		Last Modified: Thu, 22 Jul 2021 01:20:16 GMT  
		Size: 51.8 MB (51841203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6182a456504bb119011b721ede5d1e6cf4d0621447465d80cc1d4e53c0ef95e6`  
		Last Modified: Fri, 23 Jul 2021 02:05:30 GMT  
		Size: 68.7 MB (68749967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd99f184fbfe112a868508bdb8b9e5bb8c286e730654819ca87a828d9d73023`  
		Last Modified: Fri, 23 Jul 2021 02:05:40 GMT  
		Size: 134.8 MB (134784854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af0744d44b1298594fb21df479216059637960aa9afd2363cc2b0b1ba7dd1f49`  
		Last Modified: Fri, 23 Jul 2021 02:05:19 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-buster` - linux; arm variant v5

```console
$ docker pull golang@sha256:807072763450124efc0754f2a5d441d729d5c5ce3d95ebc7766e1854caf17900
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272220590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfd446be29ad4906fecdd6249626033f8429f61d833f1fdb9acee650649df4b3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:49:34 GMT
ADD file:4a4158b5432e31cd686b7b2874c22d86a381ac71c3146fe6746501db3d216b41 in / 
# Thu, 22 Jul 2021 00:49:35 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 02:03:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 02:03:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 02:04:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 16:11:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 16:11:20 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Aug 2021 02:48:32 GMT
ENV GOLANG_VERSION=1.17rc2
# Tue, 03 Aug 2021 02:52:17 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.17rc2.linux-amd64.tar.gz'; 			sha256='328235edc7c7d2a51d6c6cb4d7ff97e97357654ef9e1098b9a4603a9d278ad04'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17rc2.linux-armv6l.tar.gz'; 			sha256='4820fcd80b47e7d7dc1f15343c4fb59e66183cef9dadb3d3ac10f82615ad2141'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17rc2.linux-arm64.tar.gz'; 			sha256='4e1b335c53bf28cd20c5f7f2f7e79187b93e71c1d027448e313097785efb673d'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17rc2.linux-386.tar.gz'; 			sha256='273fd4647d2311e3044d3d937eedbee91477317d867b6c81636fdc0a9ba7f947'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17rc2.linux-ppc64le.tar.gz'; 			sha256='57fd15f97e4fccc3227d07423baca2b3e44fb2c1b12a35f8cda8a453867ca1b6'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17rc2.linux-s390x.tar.gz'; 			sha256='be3a78ae162eac193fc66b0ed50f56c75c5a1506c6b631a1f2af3d4e700816fe'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17rc2.src.tar.gz'; 		sha256='5ab21d75552390c63087518e4eba2972fb009aea97ff2bcc42dff264c5f46fe9'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Tue, 03 Aug 2021 02:52:18 GMT
ENV GOPATH=/go
# Tue, 03 Aug 2021 02:52:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Aug 2021 02:52:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 03 Aug 2021 02:52:22 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cd9bc325fb9e2673d4a4f97499e5ac67f82d24eef19ed2cb8d13af9c9256d20c`  
		Last Modified: Thu, 22 Jul 2021 01:01:22 GMT  
		Size: 48.2 MB (48153246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6ac5ad14f3066e98bd031f59bcd25af51c46975f1f67aa9e984aae49997f855`  
		Last Modified: Thu, 22 Jul 2021 02:21:02 GMT  
		Size: 7.4 MB (7376533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3538b6814e6bbc64643ef42ffb80c592cecc6833f8c77baa213b7d572de2f060`  
		Last Modified: Thu, 22 Jul 2021 02:21:02 GMT  
		Size: 9.7 MB (9687577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e98fc7d7506f4cd2a0d1ab64ad0e0a5e9863175a5bcadf61c19a25091d861d34`  
		Last Modified: Thu, 22 Jul 2021 02:21:56 GMT  
		Size: 49.6 MB (49575389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0603fa664f95d8074de109c383370a08008de46caf8d285bdc49edb42461b128`  
		Last Modified: Thu, 22 Jul 2021 16:23:47 GMT  
		Size: 52.1 MB (52056868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b3691033b113a090c2169fc9a7651f6ad451286ad85afdcc8b3e8ccabc4fbf`  
		Last Modified: Tue, 03 Aug 2021 02:55:18 GMT  
		Size: 105.4 MB (105370822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3fec79596bda4cc4a54ab738074ef1c4cee61f9b0b4853ee0da99111416fea`  
		Last Modified: Tue, 03 Aug 2021 02:54:11 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-buster` - linux; arm variant v7

```console
$ docker pull golang@sha256:11d2858063356b7cbc69e0d6db4508c49f5641aa55a6ec72ca5f5c2f92af826a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.0 MB (266040977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aea05223a27b03cd9a53ff9c39a9285e6f54c35e5fa1ab0a894640914ffc6320`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 02:03:13 GMT
ADD file:c33137dc0d277fe210ea6387a8be105c625fdf777a541a6392896766df9919d4 in / 
# Thu, 22 Jul 2021 02:03:14 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 04:14:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 04:15:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 04:15:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 04:46:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 04:46:10 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jul 2021 04:46:11 GMT
ENV GOLANG_VERSION=1.17rc1
# Fri, 23 Jul 2021 04:46:41 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.17rc1.linux-amd64.tar.gz'; 			sha256='bfbd3881a01ca3826777b1c40f241acacd45b14730d373259cd673d74e15e534'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17rc1.linux-armv6l.tar.gz'; 			sha256='1fd5c3733d6fab5ebcb3ca6ae2b478d370bb0638ba3966284ed7e7aa97acfc8a'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17rc1.linux-arm64.tar.gz'; 			sha256='7498e426ce814a94a1d271d6bb80b9a2cf8c77ec49df531c57bd7a9ff82cfa4e'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17rc1.linux-386.tar.gz'; 			sha256='e9b78a4bd98165b86bb887643f58cc0464cc7ff7fae12516fc43114809c71e07'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17rc1.linux-ppc64le.tar.gz'; 			sha256='d3aec884d6cbb8504bb25591a780759dd0ea5d9ede2a5e6af1dfe210df0a60f1'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17rc1.linux-s390x.tar.gz'; 			sha256='23318ad51bd3d164aed307b500b9e89174e7df425a0cd03e619b65bbd65d6b19'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17rc1.src.tar.gz'; 		sha256='0d63be0f3abc79d35efcb60dfce4445e64bb1ea194edcfd9783a76316b7e85e2'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 23 Jul 2021 04:46:43 GMT
ENV GOPATH=/go
# Fri, 23 Jul 2021 04:46:43 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jul 2021 04:46:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 23 Jul 2021 04:46:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ff16e408fd8b8191145782047ebc0c76176550d844743a679143d53a164bea21`  
		Last Modified: Thu, 22 Jul 2021 02:15:33 GMT  
		Size: 45.9 MB (45917250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7701a3a4dc54422c371762f5416afea6835e02e9db10fd686f73159ec84ec2f7`  
		Last Modified: Thu, 22 Jul 2021 04:35:32 GMT  
		Size: 7.1 MB (7124233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8651c1854c791264fe60acc8ab39e9b914dc3258a9aa42509f1c35ce32a880d`  
		Last Modified: Thu, 22 Jul 2021 04:35:32 GMT  
		Size: 9.3 MB (9343793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14bda9bdbd404cfcf13425f9c6273b254196ada60d6315690312688674624a7`  
		Last Modified: Thu, 22 Jul 2021 04:36:20 GMT  
		Size: 47.4 MB (47356980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554e943d351eb3a69051efb53627557f7db7ba465d51dd6cdec7b91c291f379a`  
		Last Modified: Fri, 23 Jul 2021 04:56:32 GMT  
		Size: 53.2 MB (53222447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd4d6d29460ee88e5c020549fbc7faf50343fd153dc67d8af2e0811edcf55af`  
		Last Modified: Fri, 23 Jul 2021 04:57:11 GMT  
		Size: 103.1 MB (103076120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0a6f1915b20c686fab85271c9b4dc406b6edbcd534520d4aa71550d956f990`  
		Last Modified: Fri, 23 Jul 2021 04:56:04 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-buster` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:d55c714a216d5c59a8f592274d59e5b75db28aa7f5b6e3a8ca5a587b1bd66149
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.3 MB (284283694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe9f13c7b5b10c0bf7be2bf1ae78906645548fe86daa325b6ef16c2a099910d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:39:59 GMT
ADD file:3e8e075f08a6b727602af05c539f43648a48663cbb3a88eeba310cfc32c01d78 in / 
# Thu, 22 Jul 2021 00:40:00 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 01:15:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:16:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 01:16:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 13:32:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 13:32:20 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Aug 2021 02:39:55 GMT
ENV GOLANG_VERSION=1.17rc2
# Tue, 03 Aug 2021 02:40:16 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.17rc2.linux-amd64.tar.gz'; 			sha256='328235edc7c7d2a51d6c6cb4d7ff97e97357654ef9e1098b9a4603a9d278ad04'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17rc2.linux-armv6l.tar.gz'; 			sha256='4820fcd80b47e7d7dc1f15343c4fb59e66183cef9dadb3d3ac10f82615ad2141'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17rc2.linux-arm64.tar.gz'; 			sha256='4e1b335c53bf28cd20c5f7f2f7e79187b93e71c1d027448e313097785efb673d'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17rc2.linux-386.tar.gz'; 			sha256='273fd4647d2311e3044d3d937eedbee91477317d867b6c81636fdc0a9ba7f947'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17rc2.linux-ppc64le.tar.gz'; 			sha256='57fd15f97e4fccc3227d07423baca2b3e44fb2c1b12a35f8cda8a453867ca1b6'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17rc2.linux-s390x.tar.gz'; 			sha256='be3a78ae162eac193fc66b0ed50f56c75c5a1506c6b631a1f2af3d4e700816fe'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17rc2.src.tar.gz'; 		sha256='5ab21d75552390c63087518e4eba2972fb009aea97ff2bcc42dff264c5f46fe9'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Tue, 03 Aug 2021 02:40:17 GMT
ENV GOPATH=/go
# Tue, 03 Aug 2021 02:40:17 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Aug 2021 02:40:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 03 Aug 2021 02:40:18 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d272b0d8f7c4fd0caf0ef022ce544cfe3800e349a73b585f82837e6526a4247e`  
		Last Modified: Thu, 22 Jul 2021 00:45:18 GMT  
		Size: 49.2 MB (49222109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81fabd82f026fa10e0e0341fa3d6d3112de04413ea6c46e72bcc1dca40d924aa`  
		Last Modified: Thu, 22 Jul 2021 01:25:00 GMT  
		Size: 7.7 MB (7694906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0193c0cdceae23cd0e13721651d74f409440171fe8a1c8b521616b6ed29db6e1`  
		Last Modified: Thu, 22 Jul 2021 01:25:00 GMT  
		Size: 10.0 MB (9984335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:967a8f1385966af47c9f250997e3158c319d498adc004c91570f770ceac5045a`  
		Last Modified: Thu, 22 Jul 2021 01:25:24 GMT  
		Size: 52.2 MB (52167528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f10b34911491399aa2caeb545e897b4fd44568636b77f650887a40f2e08e4e1`  
		Last Modified: Thu, 22 Jul 2021 13:36:49 GMT  
		Size: 62.6 MB (62616191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ee2b3d6235a514f07598f7fb2ac40af7019842dac71f49a72b7e18a14142e4`  
		Last Modified: Tue, 03 Aug 2021 02:47:25 GMT  
		Size: 102.6 MB (102598468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b2866678cc527db60f0403fb1758331c93f0ca0b3c30e4312b99d1debf37ad`  
		Last Modified: Tue, 03 Aug 2021 02:47:09 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-buster` - linux; 386

```console
$ docker pull golang@sha256:417ee4a93ec91f9ccba5d0bef81e79a5a073f98faf1cac02c0076c78f543bba5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.2 MB (302199656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41bcbc20e5f62414550f70be86a86446c2a8c7074476acc0bc1c782596384cd9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:39:33 GMT
ADD file:574afb2f0b9121fa552563f323a2edd9a3aa71fc927a280c3eb9cbbf944a12ff in / 
# Thu, 22 Jul 2021 00:39:34 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 04:05:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 04:05:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 04:05:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 17:28:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 17:28:04 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Aug 2021 02:39:07 GMT
ENV GOLANG_VERSION=1.17rc2
# Tue, 03 Aug 2021 02:39:22 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.17rc2.linux-amd64.tar.gz'; 			sha256='328235edc7c7d2a51d6c6cb4d7ff97e97357654ef9e1098b9a4603a9d278ad04'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17rc2.linux-armv6l.tar.gz'; 			sha256='4820fcd80b47e7d7dc1f15343c4fb59e66183cef9dadb3d3ac10f82615ad2141'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17rc2.linux-arm64.tar.gz'; 			sha256='4e1b335c53bf28cd20c5f7f2f7e79187b93e71c1d027448e313097785efb673d'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17rc2.linux-386.tar.gz'; 			sha256='273fd4647d2311e3044d3d937eedbee91477317d867b6c81636fdc0a9ba7f947'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17rc2.linux-ppc64le.tar.gz'; 			sha256='57fd15f97e4fccc3227d07423baca2b3e44fb2c1b12a35f8cda8a453867ca1b6'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17rc2.linux-s390x.tar.gz'; 			sha256='be3a78ae162eac193fc66b0ed50f56c75c5a1506c6b631a1f2af3d4e700816fe'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17rc2.src.tar.gz'; 		sha256='5ab21d75552390c63087518e4eba2972fb009aea97ff2bcc42dff264c5f46fe9'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Tue, 03 Aug 2021 02:39:23 GMT
ENV GOPATH=/go
# Tue, 03 Aug 2021 02:39:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Aug 2021 02:39:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 03 Aug 2021 02:39:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:276c935c592dc1b2a80709bfb684b8cadd019d62fed321da14653e74bc260bd2`  
		Last Modified: Thu, 22 Jul 2021 00:45:59 GMT  
		Size: 51.2 MB (51206749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74777b942e5ddcca1441a21360061ce9f880ebd5f5020bd1f8480c09ec3c9a1`  
		Last Modified: Thu, 22 Jul 2021 04:15:32 GMT  
		Size: 8.0 MB (7998524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f821b4d53bda0dd46941c09587233f0b5d34c76bd3efb4d2d0766dddea8f99`  
		Last Modified: Thu, 22 Jul 2021 04:15:33 GMT  
		Size: 10.3 MB (10339898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b349e22a93ae2ec7a8fb4830b9b80b272c758fbff384a0410f5c834c9c26a681`  
		Last Modified: Thu, 22 Jul 2021 04:16:00 GMT  
		Size: 53.4 MB (53437923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:479946c45602f49688fd89ae011dcae1ef8315e2d84dc6e4c3e2df15ea1f2534`  
		Last Modified: Thu, 22 Jul 2021 17:34:54 GMT  
		Size: 73.6 MB (73617644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea9726713756406faae2fd8a61c528b9cd84c63c7af9b5d790d39b1e473babc`  
		Last Modified: Tue, 03 Aug 2021 02:50:39 GMT  
		Size: 105.6 MB (105598762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f769440386d1c8ef93091bf1620b5a329ac90c36cd8ab35f8f4a3babeb5deda5`  
		Last Modified: Tue, 03 Aug 2021 02:50:19 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-buster` - linux; mips64le

```console
$ docker pull golang@sha256:442a19f124998dac4038fd5b038c575bc065f694c5609a5c12a44013d30f7e56
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.5 MB (274481842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0466b12846652db6f7fe775e38212a7244d9d7aee106f4b8b24f9bc7c4e2e5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:09:22 GMT
ADD file:1a6aa3d9fc5224e35958d4109d5bcb3afa5948beb85e45b91f46655fe8fadb2f in / 
# Thu, 22 Jul 2021 00:09:23 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 00:42:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 00:42:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 00:43:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 18:36:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 18:36:27 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 18:36:27 GMT
ENV GOLANG_VERSION=1.17rc1
# Thu, 22 Jul 2021 18:46:14 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.17rc1.linux-amd64.tar.gz'; 			sha256='bfbd3881a01ca3826777b1c40f241acacd45b14730d373259cd673d74e15e534'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17rc1.linux-armv6l.tar.gz'; 			sha256='1fd5c3733d6fab5ebcb3ca6ae2b478d370bb0638ba3966284ed7e7aa97acfc8a'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17rc1.linux-arm64.tar.gz'; 			sha256='7498e426ce814a94a1d271d6bb80b9a2cf8c77ec49df531c57bd7a9ff82cfa4e'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17rc1.linux-386.tar.gz'; 			sha256='e9b78a4bd98165b86bb887643f58cc0464cc7ff7fae12516fc43114809c71e07'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17rc1.linux-ppc64le.tar.gz'; 			sha256='d3aec884d6cbb8504bb25591a780759dd0ea5d9ede2a5e6af1dfe210df0a60f1'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17rc1.linux-s390x.tar.gz'; 			sha256='23318ad51bd3d164aed307b500b9e89174e7df425a0cd03e619b65bbd65d6b19'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17rc1.src.tar.gz'; 		sha256='0d63be0f3abc79d35efcb60dfce4445e64bb1ea194edcfd9783a76316b7e85e2'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 22 Jul 2021 18:46:16 GMT
ENV GOPATH=/go
# Thu, 22 Jul 2021 18:46:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 18:46:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 22 Jul 2021 18:46:18 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:dfc6cf8967b24f7ad8c4469c3140cf3967000ae27e3b40b7c72fb89755953841`  
		Last Modified: Thu, 22 Jul 2021 00:15:25 GMT  
		Size: 49.1 MB (49080577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c97f1ec44468b6cf3c95775fd68ad34176e3f3f5b114e01ef45fda232435a0ee`  
		Last Modified: Thu, 22 Jul 2021 00:54:11 GMT  
		Size: 7.3 MB (7252390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5a98fef30417ecbf0d84d2f4e0a5d8c4c745505f4453d9d128eaabe85f0caa`  
		Last Modified: Thu, 22 Jul 2021 00:54:11 GMT  
		Size: 10.0 MB (10016296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d36b0ec1b127ef255da5d2ac89935eebf1177a48ee713fa2c190f0357961a9c`  
		Last Modified: Thu, 22 Jul 2021 00:55:01 GMT  
		Size: 50.8 MB (50844871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4efd8c3e0917726909d66a1120a3edfe62a1786d35c564dec6a6af02454cda92`  
		Last Modified: Thu, 22 Jul 2021 19:03:17 GMT  
		Size: 54.7 MB (54668722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e810c89e5ef3d4a368edd973bc3e92745bb3d5781f4954a33515ee1f12751437`  
		Last Modified: Thu, 22 Jul 2021 19:03:48 GMT  
		Size: 102.6 MB (102618860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b87b77ee8f21a288e248a7c82699775475155b49768c07b2aa3ab302c00a867`  
		Last Modified: Thu, 22 Jul 2021 19:02:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-buster` - linux; ppc64le

```console
$ docker pull golang@sha256:1a4e719174d085c7909fa30728a4588ea9f7c6d1916c3c1ffe2d5d3eacecdcdb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.3 MB (305309367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b623113ffc3e4806e9c45c0c40d77118c85f917c1a71abe2d384d9188d502d5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:18:15 GMT
ADD file:e6b00a20c003d499ec3793592cb620a450afe5de34f408e897ae9ea6efde50ea in / 
# Thu, 22 Jul 2021 00:18:25 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 04:03:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 04:04:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 04:06:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 04:30:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 04:30:58 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jul 2021 04:31:14 GMT
ENV GOLANG_VERSION=1.17rc1
# Fri, 23 Jul 2021 04:32:03 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.17rc1.linux-amd64.tar.gz'; 			sha256='bfbd3881a01ca3826777b1c40f241acacd45b14730d373259cd673d74e15e534'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17rc1.linux-armv6l.tar.gz'; 			sha256='1fd5c3733d6fab5ebcb3ca6ae2b478d370bb0638ba3966284ed7e7aa97acfc8a'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17rc1.linux-arm64.tar.gz'; 			sha256='7498e426ce814a94a1d271d6bb80b9a2cf8c77ec49df531c57bd7a9ff82cfa4e'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17rc1.linux-386.tar.gz'; 			sha256='e9b78a4bd98165b86bb887643f58cc0464cc7ff7fae12516fc43114809c71e07'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17rc1.linux-ppc64le.tar.gz'; 			sha256='d3aec884d6cbb8504bb25591a780759dd0ea5d9ede2a5e6af1dfe210df0a60f1'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17rc1.linux-s390x.tar.gz'; 			sha256='23318ad51bd3d164aed307b500b9e89174e7df425a0cd03e619b65bbd65d6b19'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17rc1.src.tar.gz'; 		sha256='0d63be0f3abc79d35efcb60dfce4445e64bb1ea194edcfd9783a76316b7e85e2'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 23 Jul 2021 04:32:29 GMT
ENV GOPATH=/go
# Fri, 23 Jul 2021 04:32:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jul 2021 04:32:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 23 Jul 2021 04:32:58 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fdbf50ea37550aa240918e3856b527a5dcc59fb570024ad98c902fe59e2ffd85`  
		Last Modified: Thu, 22 Jul 2021 00:27:11 GMT  
		Size: 54.2 MB (54182444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c4eb1cdb7dec331ac914405cf72cda55e246497aa6cdfce759e808d8b0ef32`  
		Last Modified: Thu, 22 Jul 2021 05:13:39 GMT  
		Size: 8.3 MB (8271846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1473db4da98c45802b5d0ee67cc543db64220182999ed71199a61f006246bb4`  
		Last Modified: Thu, 22 Jul 2021 05:13:37 GMT  
		Size: 10.7 MB (10727883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074eb7243d00a87169e9668977de9e6f8c1b4add7e5ee0b9a74e679a90f8abb3`  
		Last Modified: Thu, 22 Jul 2021 05:14:59 GMT  
		Size: 57.5 MB (57457626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7d28b1f45661e33c8c72a41565f5fa09f8856efaa0fc5a8eb90fc4532d5717`  
		Last Modified: Fri, 23 Jul 2021 04:47:39 GMT  
		Size: 73.7 MB (73659587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daef75d2d6219b65bf7501f8e024a8862fddb3632f40fef1807f53b4415f526f`  
		Last Modified: Fri, 23 Jul 2021 04:47:44 GMT  
		Size: 101.0 MB (101009824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c619c7f995e9bba99e3553616d8e01ac24cab659a1d4e4dd9bf3784f1e30512`  
		Last Modified: Fri, 23 Jul 2021 04:47:26 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-buster` - linux; s390x

```console
$ docker pull golang@sha256:bafea0de10646ee52de8365ffd8caf5867e1ec4fd0d39e9f6e5db7f730eb3a02
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.3 MB (280253782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213d3858e5d333d0d1955da281676d28c8911c1f6da0bd93b660855c6b4ca1f9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:42:21 GMT
ADD file:0862dc2e420958057c0edfbacc39968850751ffdec84962ab8577b7787c5296f in / 
# Thu, 22 Jul 2021 00:42:26 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 01:11:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:11:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 01:12:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 21:21:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 21:21:32 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Aug 2021 02:41:39 GMT
ENV GOLANG_VERSION=1.17rc2
# Tue, 03 Aug 2021 02:41:58 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.17rc2.linux-amd64.tar.gz'; 			sha256='328235edc7c7d2a51d6c6cb4d7ff97e97357654ef9e1098b9a4603a9d278ad04'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17rc2.linux-armv6l.tar.gz'; 			sha256='4820fcd80b47e7d7dc1f15343c4fb59e66183cef9dadb3d3ac10f82615ad2141'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17rc2.linux-arm64.tar.gz'; 			sha256='4e1b335c53bf28cd20c5f7f2f7e79187b93e71c1d027448e313097785efb673d'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17rc2.linux-386.tar.gz'; 			sha256='273fd4647d2311e3044d3d937eedbee91477317d867b6c81636fdc0a9ba7f947'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17rc2.linux-ppc64le.tar.gz'; 			sha256='57fd15f97e4fccc3227d07423baca2b3e44fb2c1b12a35f8cda8a453867ca1b6'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17rc2.linux-s390x.tar.gz'; 			sha256='be3a78ae162eac193fc66b0ed50f56c75c5a1506c6b631a1f2af3d4e700816fe'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17rc2.src.tar.gz'; 		sha256='5ab21d75552390c63087518e4eba2972fb009aea97ff2bcc42dff264c5f46fe9'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Tue, 03 Aug 2021 02:42:04 GMT
ENV GOPATH=/go
# Tue, 03 Aug 2021 02:42:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Aug 2021 02:42:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 03 Aug 2021 02:42:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8776c37054ddd28ba8fe526b8dbc08bf7b521ae9ddb8eacd008d05185571cde0`  
		Last Modified: Thu, 22 Jul 2021 00:47:50 GMT  
		Size: 49.0 MB (49003783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c06f635d71fe906f56e25278d5659aa940f095c1ecf199e41436e197534383a`  
		Last Modified: Thu, 22 Jul 2021 01:27:40 GMT  
		Size: 7.4 MB (7400582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f57129f34059279bed7373d2b35f16c94df2418b85c5ae20dc715f2e1999498`  
		Last Modified: Thu, 22 Jul 2021 01:27:41 GMT  
		Size: 9.9 MB (9883324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f6521600d1dbe8e9e84511427b15a7cb2dd42039504bb9679b6ed7e7ee0dca`  
		Last Modified: Thu, 22 Jul 2021 01:28:00 GMT  
		Size: 51.4 MB (51380867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1228c41a068ba9c3aca67ff810dadc0c8a62694a090ea82e610e8728cfbbb031`  
		Last Modified: Thu, 22 Jul 2021 21:28:50 GMT  
		Size: 56.8 MB (56817857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f71b12c4a7c631b9ea716a84b8e727503012b9795bb8fea8e4f10182848836b`  
		Last Modified: Tue, 03 Aug 2021 02:49:03 GMT  
		Size: 105.8 MB (105767213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:926a3da96ae1ca8372386896a9a535dd6c647638d8f2f437b02ff1dc72d8ff4d`  
		Last Modified: Tue, 03 Aug 2021 02:48:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
