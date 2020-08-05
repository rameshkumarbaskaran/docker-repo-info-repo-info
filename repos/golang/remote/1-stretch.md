## `golang:1-stretch`

```console
$ docker pull golang@sha256:10cdbb38bb330075f7787533596e0fa2d2cf5eb9d24b75aa80987ebfc431a75a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `golang:1-stretch` - linux; amd64

```console
$ docker pull golang@sha256:b0ef5815a60d18d8c2f06fbbc9c4a7065f6faa0453fe21e777a33caecb7dc468
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.0 MB (292046097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e7575aea1b366bd3a17d179f0e3c90e50abe50c4e4eea4ca8149430be4a3e2a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 15:45:32 GMT
ADD file:a28d8a949b7577768d87fcbac346797fc5f7bad0539625339edcd09a32d6bf77 in / 
# Tue, 04 Aug 2020 15:45:33 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 23:35:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:36:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 04 Aug 2020 23:36:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 10:32:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 10:32:05 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Aug 2020 10:32:05 GMT
ENV GOLANG_VERSION=1.14.6
# Wed, 05 Aug 2020 10:32:15 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='5c566ddc2e0bcfc25c26a5dc44a440fcc0177f7350c1f01952b34d5989a0d287' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='cab39cc0fdf9731476a339af9d7bcd8fc661bfa323abb1ce9d1633fb31daeb07' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='291bccfd7d7f1915599bbcc90e49d9fccfcb0004b7c62a2f5cdf0f96a09d6a3e' ;; 		i386) goRelArch='linux-386'; goRelSha256='17b2c4e26bd3a82a0a44499ae2d36e3f2155d0fe2f6b9a14ac6b7c5afac3ca6a' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='8eb4c84e7b6aa9edb966c467dd6764d131a57d27afbd87cc8f6d10535df9e898' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='cb1f2d001ce15e51f7c4bd43f15045ea23d49268010bb981110242a532138749' ;; 		*) goRelArch='src'; goRelSha256='73fc9d781815d411928eccb92bf20d5b4264797be69410eac854babe44c94c09'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 		eval "$goEnv"; 		[ -n "$GOOS" ]; 		[ -n "$GOARCH" ]; 		( 			cd /usr/local/go/src; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 05 Aug 2020 10:32:17 GMT
ENV GOPATH=/go
# Wed, 05 Aug 2020 10:32:17 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Aug 2020 10:32:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 05 Aug 2020 10:32:18 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:419e7ae5bb1e4875c367f3249b7bb7f8f39dd27dfceb4ee9d6a92191ed1c452f`  
		Last Modified: Tue, 04 Aug 2020 15:52:05 GMT  
		Size: 45.4 MB (45366706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848839e0cd3b3acc96db8a39c4520a40f98dc8f3a2a5f80b575ff4a1c88f1fcf`  
		Last Modified: Tue, 04 Aug 2020 23:42:18 GMT  
		Size: 10.8 MB (10750599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de30e8b35015c7302e071e9c2b449290f270feaf2a419f6466a555b6907e7d72`  
		Last Modified: Tue, 04 Aug 2020 23:42:17 GMT  
		Size: 4.3 MB (4339945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258fdea6ea480a97ea4bfe331e7dc9e027edbb0a18781d0d85ca1acc80b7a596`  
		Last Modified: Tue, 04 Aug 2020 23:42:32 GMT  
		Size: 50.1 MB (50086827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32b6789636b814a54ae670f0a44ea5c8bf7a1139c04b908731e951874c8ebd1`  
		Last Modified: Wed, 05 Aug 2020 10:34:30 GMT  
		Size: 57.8 MB (57754335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986921e920983064015a5861ba601423fe49fc67d4ad2d6a9e487ae6a2464d1a`  
		Last Modified: Wed, 05 Aug 2020 10:34:40 GMT  
		Size: 123.7 MB (123747560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc9f204b72379d4bc76b11bc6ccdac940ee4cc6f5753a88f005a3788215c27e8`  
		Last Modified: Wed, 05 Aug 2020 10:34:19 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-stretch` - linux; arm variant v7

```console
$ docker pull golang@sha256:6a43a34c7f73b848a569adbff71194fea277568b29118d739ca5eb31655bf3d7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.8 MB (249794964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eddea6a5888e79c3aad3c9953828cabfe299530122e5907b5abe16b3c469ffd2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 05:01:04 GMT
ADD file:0ba6f3203fb10e66124d03088d234e92fc908c572ec7eed268e866623a383a7d in / 
# Tue, 04 Aug 2020 05:01:07 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 08:16:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 08:16:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 04 Aug 2020 08:18:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 01:42:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 01:42:40 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Aug 2020 01:42:41 GMT
ENV GOLANG_VERSION=1.14.6
# Wed, 05 Aug 2020 01:43:06 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='5c566ddc2e0bcfc25c26a5dc44a440fcc0177f7350c1f01952b34d5989a0d287' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='cab39cc0fdf9731476a339af9d7bcd8fc661bfa323abb1ce9d1633fb31daeb07' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='291bccfd7d7f1915599bbcc90e49d9fccfcb0004b7c62a2f5cdf0f96a09d6a3e' ;; 		i386) goRelArch='linux-386'; goRelSha256='17b2c4e26bd3a82a0a44499ae2d36e3f2155d0fe2f6b9a14ac6b7c5afac3ca6a' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='8eb4c84e7b6aa9edb966c467dd6764d131a57d27afbd87cc8f6d10535df9e898' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='cb1f2d001ce15e51f7c4bd43f15045ea23d49268010bb981110242a532138749' ;; 		*) goRelArch='src'; goRelSha256='73fc9d781815d411928eccb92bf20d5b4264797be69410eac854babe44c94c09'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 		eval "$goEnv"; 		[ -n "$GOOS" ]; 		[ -n "$GOARCH" ]; 		( 			cd /usr/local/go/src; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 05 Aug 2020 01:43:09 GMT
ENV GOPATH=/go
# Wed, 05 Aug 2020 01:43:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Aug 2020 01:43:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 05 Aug 2020 01:43:17 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:323178d00ec2c5eb5ffb9cb696a52eaf8683dcf2eb605c742da2953556f06e37`  
		Last Modified: Tue, 04 Aug 2020 05:08:40 GMT  
		Size: 42.1 MB (42111382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b4e15a79453f6ae10815d79c8f4590aef2f1ac2979c192ff7f1ed0fbf04e60`  
		Last Modified: Tue, 04 Aug 2020 08:30:43 GMT  
		Size: 9.4 MB (9443881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caf9cb1ef704caf3af8a2ed43dc12884b4f74ac867ce95f60bd8996f51fde770`  
		Last Modified: Tue, 04 Aug 2020 08:30:41 GMT  
		Size: 3.9 MB (3918490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ae4cf51f1ae7af0566bc381b7fdc344ae6a916df2554156029039b4925d30c`  
		Last Modified: Tue, 04 Aug 2020 08:31:09 GMT  
		Size: 46.4 MB (46415465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128797a1aa794ca62cfffc928723ecde348b31a22dc1c199c8655a3c2f595866`  
		Last Modified: Wed, 05 Aug 2020 01:47:15 GMT  
		Size: 46.1 MB (46090847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865a74e4bd66a0c0012667370951cc00f7ce4e6bd89f1505750d91aeb3c427a6`  
		Last Modified: Wed, 05 Aug 2020 01:47:35 GMT  
		Size: 101.8 MB (101814743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a6e7d3786645579556cefe34d7e2e423963d88a639d687134875c636414393`  
		Last Modified: Wed, 05 Aug 2020 01:47:02 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-stretch` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:921b19cf2cebc2ffcf0bbc371f24ffabe365db0b63a41a328b5dd2c86f70ae40
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.2 MB (255234766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7a07e7e8d79c90cb44eb3cdc31834fa336bfc75846956d3eac9e89e93bf2cfb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 06:59:38 GMT
ADD file:0a7a65de4c9dc6ea7f7ac97362a47b82a02a45ecab668ddc84cfd011dad26d33 in / 
# Tue, 04 Aug 2020 06:59:41 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 11:16:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 11:16:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 04 Aug 2020 11:17:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 07:20:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 07:20:52 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Aug 2020 07:20:53 GMT
ENV GOLANG_VERSION=1.14.6
# Wed, 05 Aug 2020 07:21:10 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='5c566ddc2e0bcfc25c26a5dc44a440fcc0177f7350c1f01952b34d5989a0d287' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='cab39cc0fdf9731476a339af9d7bcd8fc661bfa323abb1ce9d1633fb31daeb07' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='291bccfd7d7f1915599bbcc90e49d9fccfcb0004b7c62a2f5cdf0f96a09d6a3e' ;; 		i386) goRelArch='linux-386'; goRelSha256='17b2c4e26bd3a82a0a44499ae2d36e3f2155d0fe2f6b9a14ac6b7c5afac3ca6a' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='8eb4c84e7b6aa9edb966c467dd6764d131a57d27afbd87cc8f6d10535df9e898' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='cb1f2d001ce15e51f7c4bd43f15045ea23d49268010bb981110242a532138749' ;; 		*) goRelArch='src'; goRelSha256='73fc9d781815d411928eccb92bf20d5b4264797be69410eac854babe44c94c09'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 		eval "$goEnv"; 		[ -n "$GOOS" ]; 		[ -n "$GOARCH" ]; 		( 			cd /usr/local/go/src; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 05 Aug 2020 07:21:12 GMT
ENV GOPATH=/go
# Wed, 05 Aug 2020 07:21:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Aug 2020 07:21:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 05 Aug 2020 07:21:16 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:708f9b01fc1a5dff70f7d40443ac7dd0ee1d0ae93202b6f305f4e3627cea7d22`  
		Last Modified: Tue, 04 Aug 2020 07:06:12 GMT  
		Size: 43.2 MB (43171643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06dc3a0299d558e9f611edd56658d792af018276662c8c30d86476a05c18b00b`  
		Last Modified: Tue, 04 Aug 2020 11:26:22 GMT  
		Size: 9.7 MB (9700890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7feaa2634e51f929e9ca86765cd5579cdf0809084c80d6787166627ca2aed6d4`  
		Last Modified: Tue, 04 Aug 2020 11:26:21 GMT  
		Size: 4.1 MB (4094122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5d948bc7089eee9551a072ac758688696cf87a38dce63eb5f20b8dcdb94436`  
		Last Modified: Tue, 04 Aug 2020 11:26:45 GMT  
		Size: 48.0 MB (48041118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c24fd75724c702a965c69e5277511924c075269631875bf1eb0479e58d07f5`  
		Last Modified: Wed, 05 Aug 2020 07:24:38 GMT  
		Size: 49.2 MB (49159332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3bf5b2e0e3b494027b85c3d13b32680281173c61e50a04bfbb41498d30ab6df`  
		Last Modified: Wed, 05 Aug 2020 07:24:51 GMT  
		Size: 101.1 MB (101067506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef5113f707790afc471f746ffadfd8d22fb7ced821eb6d68c92c51f78b79cee`  
		Last Modified: Wed, 05 Aug 2020 07:24:26 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-stretch` - linux; 386

```console
$ docker pull golang@sha256:cc1a80fbfb8ebbf681330f4a6b3891b829e8c25e3595e30da6fb1191a1f44015
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280200910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3421b20d405db4127c5f063ebb81f99425a88412831d72e11ae28de9869f5150`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 03:39:59 GMT
ADD file:af30f23f89d9bbdd6ad60199f3d978a5e426835c6138e0c76a3453680945a121 in / 
# Tue, 04 Aug 2020 03:39:59 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 08:21:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 08:21:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 04 Aug 2020 08:21:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 18:44:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 18:44:49 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Aug 2020 18:44:50 GMT
ENV GOLANG_VERSION=1.14.6
# Tue, 04 Aug 2020 18:45:02 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='5c566ddc2e0bcfc25c26a5dc44a440fcc0177f7350c1f01952b34d5989a0d287' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='cab39cc0fdf9731476a339af9d7bcd8fc661bfa323abb1ce9d1633fb31daeb07' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='291bccfd7d7f1915599bbcc90e49d9fccfcb0004b7c62a2f5cdf0f96a09d6a3e' ;; 		i386) goRelArch='linux-386'; goRelSha256='17b2c4e26bd3a82a0a44499ae2d36e3f2155d0fe2f6b9a14ac6b7c5afac3ca6a' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='8eb4c84e7b6aa9edb966c467dd6764d131a57d27afbd87cc8f6d10535df9e898' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='cb1f2d001ce15e51f7c4bd43f15045ea23d49268010bb981110242a532138749' ;; 		*) goRelArch='src'; goRelSha256='73fc9d781815d411928eccb92bf20d5b4264797be69410eac854babe44c94c09'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				goEnv="$(go env | sed -rn -e '/^GO(OS|ARCH|ARM|386)=/s//export \0/p')"; 		eval "$goEnv"; 		[ -n "$GOOS" ]; 		[ -n "$GOARCH" ]; 		( 			cd /usr/local/go/src; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Tue, 04 Aug 2020 18:45:03 GMT
ENV GOPATH=/go
# Tue, 04 Aug 2020 18:45:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Aug 2020 18:45:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 04 Aug 2020 18:45:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:36eaaca1a8d1677d2d2aa93f595d838e71ccbe4254f548ff566f97e8d555df1c`  
		Last Modified: Tue, 04 Aug 2020 03:45:28 GMT  
		Size: 46.1 MB (46086777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:312e98903306441f0b9bd43306e20722d14f9f02f55de10e037f31f8e9887d06`  
		Last Modified: Tue, 04 Aug 2020 08:30:08 GMT  
		Size: 10.8 MB (10773882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98fa371da331bdfaab943357b965c1839c24c25c15a78aaa7180325db8fb59ca`  
		Last Modified: Tue, 04 Aug 2020 08:30:06 GMT  
		Size: 4.6 MB (4561115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b121224d37089d29e88079f00cc9ed94ee5cf4bc763184a9c90231f28a0291`  
		Last Modified: Tue, 04 Aug 2020 08:30:39 GMT  
		Size: 51.6 MB (51619972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfecd89ef84bb1f302d9835c51fe7f69081a9285401a0871beef5ee5b0ee40b6`  
		Last Modified: Tue, 04 Aug 2020 18:47:38 GMT  
		Size: 62.3 MB (62280574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b4ffc7689548ba8d650c75e698eb922d50e5a66ac2268008771b81e977e56d`  
		Last Modified: Tue, 04 Aug 2020 18:47:43 GMT  
		Size: 104.9 MB (104878464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeab7e848ba690de60dbf1222e4f5799463ad0142fc16b82ace7bd9cad70c128`  
		Last Modified: Tue, 04 Aug 2020 18:47:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
