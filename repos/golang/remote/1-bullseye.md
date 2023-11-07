## `golang:1-bullseye`

```console
$ docker pull golang@sha256:2fa733e07e0b3d41566a25c7e52f359264c7cace5d74b1b90bf1ba835f63e802
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

### `golang:1-bullseye` - linux; amd64

```console
$ docker pull golang@sha256:ea48852045248675a6f1948acc4c996b1a5de151a77213b936840bf1f82ddd02
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.5 MB (278478890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a64cc2376c85b65e2c9a14589c14cc33eaee0f230e8c2e69ba2a7f1bc56a41`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:59 GMT
ADD file:da3938f00f114fa8f5948fb7182da39c43e5ce57a334ba528681cb29aff0d2f6 in / 
# Wed, 01 Nov 2023 00:21:00 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 00:53:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 00:54:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 18:05:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 18:05:18 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Nov 2023 20:20:09 GMT
ENV GOLANG_VERSION=1.21.4
# Tue, 07 Nov 2023 20:20:18 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.4.linux-amd64.tar.gz'; 			sha256='73cac0215254d0c7d1241fa40837851f3b9a8a742d0b54714cbdfb3feaf8f0af'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.4.linux-armv6l.tar.gz'; 			sha256='6c62e89113750cc77c498194d13a03fadfda22bd2c7d44e8a826fd354db60252'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.4.linux-arm64.tar.gz'; 			sha256='ce1983a7289856c3a918e1fd26d41e072cc39f928adfb11ba1896440849b95da'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.4.linux-386.tar.gz'; 			sha256='64d3e5d295806e137c9e39d1e1f10b00a30fcd5c2f230d72b3298f579bb3c89a'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.4.linux-mips64le.tar.gz'; 			sha256='c7ce3a9dcf03322b79beda474c4a0154393d9029b48f7c2e260fb3365c8a6ad3'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.4.linux-ppc64le.tar.gz'; 			sha256='2c63b36d2adcfb22013102a2ee730f058ec2f93b9f27479793c80b2e3641783f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.4.linux-riscv64.tar.gz'; 			sha256='9695edd2109544b364daddb32816f5c7980f1f48b8490c51fa2c167f5b2eca48'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.4.linux-s390x.tar.gz'; 			sha256='7a75ba4afc7a96058ca65903d994cd862381825d7dca12b2183f087c757c26c0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.4.src.tar.gz'; 		sha256='47b26a83d2b65a3c1c1bcace273b69bee49a7a7b5168a7604ded3d26a37bd787'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		( 			. /etc/os-release; 			echo "deb https://deb.debian.org/debian $VERSION_CODENAME-backports main" > /etc/apt/sources.list.d/backports.list; 						apt-get update; 			apt-get install -y --no-install-recommends -t "$VERSION_CODENAME-backports" golang-go; 		); 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Tue, 07 Nov 2023 20:20:19 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Nov 2023 20:20:19 GMT
ENV GOPATH=/go
# Tue, 07 Nov 2023 20:20:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Nov 2023 20:20:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 07 Nov 2023 20:20:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2f088d622efd8dbaa13d01eafd0aac8f9f33bb335edd3be897ae8059338c7bf7`  
		Last Modified: Wed, 01 Nov 2023 00:25:49 GMT  
		Size: 55.1 MB (55058052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de448b80f06437f3025dcaa9285d40c9c81e4be00df1b04bd5a26fd6b9447fc8`  
		Last Modified: Wed, 01 Nov 2023 01:03:07 GMT  
		Size: 15.8 MB (15764212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e5da9a0e1f93fa4f1a07ca9a691e0d941bab6927f80157ffc14b478815f95b`  
		Last Modified: Wed, 01 Nov 2023 01:03:23 GMT  
		Size: 54.6 MB (54595619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9ba79c2095d2bd873656cfdbb6029a6db6ad6c1ca3d8a537a9c648524b1d02`  
		Last Modified: Wed, 01 Nov 2023 18:10:54 GMT  
		Size: 86.1 MB (86086117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666875e09b7299a7f8713c78b1c6c582e88a4d74c937942eaedc48eae946b1dc`  
		Last Modified: Tue, 07 Nov 2023 20:26:24 GMT  
		Size: 67.0 MB (66974733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6abaa1f850d319fee3416f4b6fccd084a1442b528aca8e339593576dfb99e1e`  
		Last Modified: Tue, 07 Nov 2023 20:26:12 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bullseye` - linux; arm variant v5

```console
$ docker pull golang@sha256:f12d0e63b11f2a68f91354ae56362b5062936fc1f28de48bd7f4ef759b5397ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.5 MB (257517348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4fc2f0dd36e8cb8d10ac3298c125af4fa9f7f93aabb5a7f65e6d18f300b4db5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:48:39 GMT
ADD file:6fcdedd346da0744f7f45d0e7df77336a37ce87345bd414bd4e198804980781e in / 
# Wed, 01 Nov 2023 00:48:40 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:57:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 02:57:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:40:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 14:40:34 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Nov 2023 20:50:40 GMT
ENV GOLANG_VERSION=1.21.4
# Tue, 07 Nov 2023 20:53:12 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.4.linux-amd64.tar.gz'; 			sha256='73cac0215254d0c7d1241fa40837851f3b9a8a742d0b54714cbdfb3feaf8f0af'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.4.linux-armv6l.tar.gz'; 			sha256='6c62e89113750cc77c498194d13a03fadfda22bd2c7d44e8a826fd354db60252'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.4.linux-arm64.tar.gz'; 			sha256='ce1983a7289856c3a918e1fd26d41e072cc39f928adfb11ba1896440849b95da'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.4.linux-386.tar.gz'; 			sha256='64d3e5d295806e137c9e39d1e1f10b00a30fcd5c2f230d72b3298f579bb3c89a'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.4.linux-mips64le.tar.gz'; 			sha256='c7ce3a9dcf03322b79beda474c4a0154393d9029b48f7c2e260fb3365c8a6ad3'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.4.linux-ppc64le.tar.gz'; 			sha256='2c63b36d2adcfb22013102a2ee730f058ec2f93b9f27479793c80b2e3641783f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.4.linux-riscv64.tar.gz'; 			sha256='9695edd2109544b364daddb32816f5c7980f1f48b8490c51fa2c167f5b2eca48'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.4.linux-s390x.tar.gz'; 			sha256='7a75ba4afc7a96058ca65903d994cd862381825d7dca12b2183f087c757c26c0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.4.src.tar.gz'; 		sha256='47b26a83d2b65a3c1c1bcace273b69bee49a7a7b5168a7604ded3d26a37bd787'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		( 			. /etc/os-release; 			echo "deb https://deb.debian.org/debian $VERSION_CODENAME-backports main" > /etc/apt/sources.list.d/backports.list; 						apt-get update; 			apt-get install -y --no-install-recommends -t "$VERSION_CODENAME-backports" golang-go; 		); 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Tue, 07 Nov 2023 20:53:14 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Nov 2023 20:53:14 GMT
ENV GOPATH=/go
# Tue, 07 Nov 2023 20:53:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Nov 2023 20:53:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 07 Nov 2023 20:53:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e0adb3cac2906548cd3544bf3c384be3e3bdca9d41c37e11c160813af74301b9`  
		Last Modified: Wed, 01 Nov 2023 00:51:49 GMT  
		Size: 52.6 MB (52563334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f1ac168a113a53eb04058318b3d7cb7470e780e76570d1454453907e7a8707`  
		Last Modified: Wed, 01 Nov 2023 03:06:05 GMT  
		Size: 15.4 MB (15374711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17505c8dbffa755d9815a1b1f2a760d22100354db441079cb21283d37a0f5cae`  
		Last Modified: Wed, 01 Nov 2023 03:06:23 GMT  
		Size: 52.3 MB (52331088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbfc3b1d0b28387cc285373fb769149ecb2e9e01c3b42773943cd7ef5a02425`  
		Last Modified: Wed, 01 Nov 2023 14:48:02 GMT  
		Size: 69.0 MB (68981214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf13ba012e1c92304c5527cbcdbe59b94d9e670d571d39c3ad1c9ac523ff53b`  
		Last Modified: Tue, 07 Nov 2023 20:58:53 GMT  
		Size: 68.3 MB (68266845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19915cb1e54eb78c40e6345597cab335fbc9f5f724d9884c83164cf1dddfeed4`  
		Last Modified: Tue, 07 Nov 2023 20:58:40 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:c09950d9c66f206cff2dea159bc1e91e06a9546887f5bdae6225c3b5917438ad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.2 MB (246199360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ed87c05b09d5644a00ca692d48064a19c15feadf65b91bb4fe99f5cf86983b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:58:01 GMT
ADD file:5e11ff51eeca3d0b7e760186b5792864fee2bfe7e8a1fa531a89870abaebfc89 in / 
# Wed, 01 Nov 2023 00:58:02 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:31:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 02:32:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 15:58:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 15:58:29 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Nov 2023 21:00:20 GMT
ENV GOLANG_VERSION=1.21.4
# Tue, 07 Nov 2023 21:00:31 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.4.linux-amd64.tar.gz'; 			sha256='73cac0215254d0c7d1241fa40837851f3b9a8a742d0b54714cbdfb3feaf8f0af'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.4.linux-armv6l.tar.gz'; 			sha256='6c62e89113750cc77c498194d13a03fadfda22bd2c7d44e8a826fd354db60252'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.4.linux-arm64.tar.gz'; 			sha256='ce1983a7289856c3a918e1fd26d41e072cc39f928adfb11ba1896440849b95da'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.4.linux-386.tar.gz'; 			sha256='64d3e5d295806e137c9e39d1e1f10b00a30fcd5c2f230d72b3298f579bb3c89a'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.4.linux-mips64le.tar.gz'; 			sha256='c7ce3a9dcf03322b79beda474c4a0154393d9029b48f7c2e260fb3365c8a6ad3'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.4.linux-ppc64le.tar.gz'; 			sha256='2c63b36d2adcfb22013102a2ee730f058ec2f93b9f27479793c80b2e3641783f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.4.linux-riscv64.tar.gz'; 			sha256='9695edd2109544b364daddb32816f5c7980f1f48b8490c51fa2c167f5b2eca48'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.4.linux-s390x.tar.gz'; 			sha256='7a75ba4afc7a96058ca65903d994cd862381825d7dca12b2183f087c757c26c0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.4.src.tar.gz'; 		sha256='47b26a83d2b65a3c1c1bcace273b69bee49a7a7b5168a7604ded3d26a37bd787'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		( 			. /etc/os-release; 			echo "deb https://deb.debian.org/debian $VERSION_CODENAME-backports main" > /etc/apt/sources.list.d/backports.list; 						apt-get update; 			apt-get install -y --no-install-recommends -t "$VERSION_CODENAME-backports" golang-go; 		); 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Tue, 07 Nov 2023 21:00:32 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Nov 2023 21:00:33 GMT
ENV GOPATH=/go
# Tue, 07 Nov 2023 21:00:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Nov 2023 21:00:33 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 07 Nov 2023 21:00:33 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:17b69ad2612f8fffb539ede3765dcc1fbd121518fd38fe89720482d622dbc960`  
		Last Modified: Wed, 01 Nov 2023 01:02:32 GMT  
		Size: 50.2 MB (50215350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0803d90cd63c47dea677f156a9802a95d09886d9a3b07415dd94b2ac199f25`  
		Last Modified: Wed, 01 Nov 2023 02:43:01 GMT  
		Size: 14.9 MB (14879723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:524b9dc19e6fd54f3a85453a84bc99da2ca6e508d91ce084872e33c6c60d774c`  
		Last Modified: Wed, 01 Nov 2023 02:43:18 GMT  
		Size: 50.4 MB (50353285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56638ea34910f330a8559a064df5e3952be998cb8c1dcb5398c69e242f77a42d`  
		Last Modified: Wed, 01 Nov 2023 16:05:33 GMT  
		Size: 65.0 MB (65006549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0671c62dbb7b9e58a52fae4f15c0eb8e890f5a1f8eec3f86c37dd90c9fe4620f`  
		Last Modified: Tue, 07 Nov 2023 21:07:00 GMT  
		Size: 65.7 MB (65744298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a137ad2b11b4b06d3b7f39e633cf84db133f77e0fa68f6b4fa3148e7be9c69`  
		Last Modified: Tue, 07 Nov 2023 21:06:41 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:533670a006038e56d69bf7a53cd27d9968c5ea0518d95a8f284a1e0eeaed6032
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.7 MB (269723179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6395f4915156499855e376253f69d3e2bdee65a39a9e7485aea979d6fd37836b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:48 GMT
ADD file:f5677286e85ce6a345c7f5937e1ec576c37228e49c0fafe33574614c81cb7f76 in / 
# Wed, 01 Nov 2023 00:39:48 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 02:06:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 02:06:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 15:35:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 15:36:00 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Nov 2023 20:39:44 GMT
ENV GOLANG_VERSION=1.21.4
# Tue, 07 Nov 2023 20:39:51 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.4.linux-amd64.tar.gz'; 			sha256='73cac0215254d0c7d1241fa40837851f3b9a8a742d0b54714cbdfb3feaf8f0af'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.4.linux-armv6l.tar.gz'; 			sha256='6c62e89113750cc77c498194d13a03fadfda22bd2c7d44e8a826fd354db60252'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.4.linux-arm64.tar.gz'; 			sha256='ce1983a7289856c3a918e1fd26d41e072cc39f928adfb11ba1896440849b95da'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.4.linux-386.tar.gz'; 			sha256='64d3e5d295806e137c9e39d1e1f10b00a30fcd5c2f230d72b3298f579bb3c89a'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.4.linux-mips64le.tar.gz'; 			sha256='c7ce3a9dcf03322b79beda474c4a0154393d9029b48f7c2e260fb3365c8a6ad3'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.4.linux-ppc64le.tar.gz'; 			sha256='2c63b36d2adcfb22013102a2ee730f058ec2f93b9f27479793c80b2e3641783f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.4.linux-riscv64.tar.gz'; 			sha256='9695edd2109544b364daddb32816f5c7980f1f48b8490c51fa2c167f5b2eca48'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.4.linux-s390x.tar.gz'; 			sha256='7a75ba4afc7a96058ca65903d994cd862381825d7dca12b2183f087c757c26c0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.4.src.tar.gz'; 		sha256='47b26a83d2b65a3c1c1bcace273b69bee49a7a7b5168a7604ded3d26a37bd787'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		( 			. /etc/os-release; 			echo "deb https://deb.debian.org/debian $VERSION_CODENAME-backports main" > /etc/apt/sources.list.d/backports.list; 						apt-get update; 			apt-get install -y --no-install-recommends -t "$VERSION_CODENAME-backports" golang-go; 		); 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Tue, 07 Nov 2023 20:39:53 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Nov 2023 20:39:53 GMT
ENV GOPATH=/go
# Tue, 07 Nov 2023 20:39:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Nov 2023 20:39:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 07 Nov 2023 20:39:53 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d42ebdfc37acca5c3acbe173ac11133e691b402003a525c2b8431baf6935291e`  
		Last Modified: Wed, 01 Nov 2023 00:43:25 GMT  
		Size: 53.7 MB (53707757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098bcc814ee5bafa2842bc45ecc3974bc4f2b66d05b05a8da5ac0c9fb91be947`  
		Last Modified: Wed, 01 Nov 2023 02:14:42 GMT  
		Size: 15.7 MB (15749872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e627bbf1475bea4dce35bb2c9ee58b6eb3be5573e4efe8bd5793ae6a1555118`  
		Last Modified: Wed, 01 Nov 2023 02:14:57 GMT  
		Size: 54.7 MB (54699568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eeaa778b1cd35a09bad85f17609ca9defc4b4bca11d7a8a87f69288d85783ee`  
		Last Modified: Wed, 01 Nov 2023 15:40:41 GMT  
		Size: 81.5 MB (81486529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c491613c242e15d74f69369aca79b34c3c2d9f869c3cff88421416451f6b3f0e`  
		Last Modified: Tue, 07 Nov 2023 20:44:47 GMT  
		Size: 64.1 MB (64079297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3dca565732329c0f7c097fc70c31f49c59898b5c8e0aa733983e6c416e8909`  
		Last Modified: Tue, 07 Nov 2023 20:44:33 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bullseye` - linux; 386

```console
$ docker pull golang@sha256:07d8e0334cbd9e21b7bb155c8f1fbe00132ec0e4705784c1a4d04130d82402c6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.2 MB (281188493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b72569c62ad19a8835cdc06f2f978444038cb112b386cb4bf61885e06e1be82c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:39:06 GMT
ADD file:4095d27bc1a281dda044919be3bb570d581df169c01f22b0963b38e0dd6d9eff in / 
# Wed, 01 Nov 2023 00:39:07 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 13:46:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 13:46:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Nov 2023 00:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Nov 2023 00:30:00 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Nov 2023 20:38:40 GMT
ENV GOLANG_VERSION=1.21.4
# Tue, 07 Nov 2023 20:38:53 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.4.linux-amd64.tar.gz'; 			sha256='73cac0215254d0c7d1241fa40837851f3b9a8a742d0b54714cbdfb3feaf8f0af'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.4.linux-armv6l.tar.gz'; 			sha256='6c62e89113750cc77c498194d13a03fadfda22bd2c7d44e8a826fd354db60252'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.4.linux-arm64.tar.gz'; 			sha256='ce1983a7289856c3a918e1fd26d41e072cc39f928adfb11ba1896440849b95da'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.4.linux-386.tar.gz'; 			sha256='64d3e5d295806e137c9e39d1e1f10b00a30fcd5c2f230d72b3298f579bb3c89a'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.4.linux-mips64le.tar.gz'; 			sha256='c7ce3a9dcf03322b79beda474c4a0154393d9029b48f7c2e260fb3365c8a6ad3'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.4.linux-ppc64le.tar.gz'; 			sha256='2c63b36d2adcfb22013102a2ee730f058ec2f93b9f27479793c80b2e3641783f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.4.linux-riscv64.tar.gz'; 			sha256='9695edd2109544b364daddb32816f5c7980f1f48b8490c51fa2c167f5b2eca48'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.4.linux-s390x.tar.gz'; 			sha256='7a75ba4afc7a96058ca65903d994cd862381825d7dca12b2183f087c757c26c0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.4.src.tar.gz'; 		sha256='47b26a83d2b65a3c1c1bcace273b69bee49a7a7b5168a7604ded3d26a37bd787'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		( 			. /etc/os-release; 			echo "deb https://deb.debian.org/debian $VERSION_CODENAME-backports main" > /etc/apt/sources.list.d/backports.list; 						apt-get update; 			apt-get install -y --no-install-recommends -t "$VERSION_CODENAME-backports" golang-go; 		); 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Tue, 07 Nov 2023 20:38:54 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Nov 2023 20:38:54 GMT
ENV GOPATH=/go
# Tue, 07 Nov 2023 20:38:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Nov 2023 20:38:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 07 Nov 2023 20:38:55 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:95d6aa56ba74b8ed0a732c4676a2c45c84a18076696d466cd9bf0b459c600e02`  
		Last Modified: Wed, 01 Nov 2023 00:43:49 GMT  
		Size: 56.0 MB (56046261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a221a3957c157fc6091d669757aa644810547d3e3fcf1e1af9da5c23408ccfd`  
		Last Modified: Wed, 01 Nov 2023 13:57:18 GMT  
		Size: 16.3 MB (16268154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ae620e9f38cdbc37cabf7785918528f2cabd2fc93a6f2df4a0536a17c985a83`  
		Last Modified: Wed, 01 Nov 2023 13:57:39 GMT  
		Size: 55.9 MB (55937130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b4204b956ed656c03072f656434a4c0a2fa7831f2f485ec175973dcf491bf21`  
		Last Modified: Thu, 02 Nov 2023 00:39:14 GMT  
		Size: 87.5 MB (87502859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc5da8a8662ce17f91ec60aad01a67dbfa488674fddb9066662d65c2abd08a6`  
		Last Modified: Tue, 07 Nov 2023 20:48:09 GMT  
		Size: 65.4 MB (65433933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf28cd57e99da5667f9ebbc14c7ea1f77c2621f76ff50a182bb5e1196e1fe4b`  
		Last Modified: Tue, 07 Nov 2023 20:47:52 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bullseye` - linux; mips64le

```console
$ docker pull golang@sha256:e5c50a2c349b548e40413fe55888d975eee2823b65cfd283d49d306748b15d18
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.2 MB (251209442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfd70a1d2fa37223c7c0cff8f2d5cc0d6ed9d3af7d75abd03f0948fb34040f56`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 01:09:34 GMT
ADD file:2c9f9140e731974a497825454c08d67829f514a83742973e30454cc905ebac6c in / 
# Wed, 01 Nov 2023 01:09:39 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 21:26:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 21:27:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Nov 2023 17:23:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Nov 2023 17:23:33 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Nov 2023 17:23:37 GMT
ENV GOLANG_VERSION=1.21.3
# Thu, 02 Nov 2023 17:24:24 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.3.linux-mips64le.tar.gz'; 			sha256='a569ffbc88b4e14cf2682f65cec950460665e4392b0d78b8868b4718c979bda8'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		( 			. /etc/os-release; 			echo "deb https://deb.debian.org/debian $VERSION_CODENAME-backports main" > /etc/apt/sources.list.d/backports.list; 						apt-get update; 			apt-get install -y --no-install-recommends -t "$VERSION_CODENAME-backports" golang-go; 		); 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Thu, 02 Nov 2023 17:24:32 GMT
ENV GOTOOLCHAIN=local
# Thu, 02 Nov 2023 17:24:39 GMT
ENV GOPATH=/go
# Thu, 02 Nov 2023 17:24:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Nov 2023 17:24:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Thu, 02 Nov 2023 17:25:01 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a10c6e715fcf314db953339b3e58b9e0167f6cd2d02bf633e20282058eb83331`  
		Last Modified: Wed, 01 Nov 2023 01:20:31 GMT  
		Size: 53.3 MB (53288991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe6d659051b6e411cbd9b3be6e727341a73a5b15c0c29975704b7249f84fd86`  
		Last Modified: Wed, 01 Nov 2023 21:57:24 GMT  
		Size: 15.5 MB (15529696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8566d8664b53694b0954345257a0d1054f4e6986ca39c2e219045fec1804bca9`  
		Last Modified: Wed, 01 Nov 2023 21:58:10 GMT  
		Size: 53.3 MB (53302576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6777947ccfb3c924fb210905ef5b7e08ccdaa988249f3612a85f6fde309ffe`  
		Last Modified: Thu, 02 Nov 2023 17:52:43 GMT  
		Size: 67.0 MB (66952818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c926b8e0354ca7824f531fb0de7cc766b76ec1f84c1e71c7bcd7fb4c882a3a`  
		Last Modified: Thu, 02 Nov 2023 17:52:49 GMT  
		Size: 62.1 MB (62135235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a564fe61c8a03849527c91462070f7e2ebb8b3ddcec08ff70b0bb028e6fb2d67`  
		Last Modified: Thu, 02 Nov 2023 17:52:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bullseye` - linux; ppc64le

```console
$ docker pull golang@sha256:cab3ed854c702b356e7da31cbd41279ebb726d48ff7491ff26c23cd516a00d2a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.2 MB (279226302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7c504bc70afe9829468af08d747e8fbafac1717632c26530a2dfe8d7944a42`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:51 GMT
ADD file:68e9024f0c99fe38d7046b4ad1aee044d14b93d248ec431380a1cefcacb7dea3 in / 
# Wed, 01 Nov 2023 00:21:54 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:27:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:28:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 13:53:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 13:53:54 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 13:53:56 GMT
ENV GOLANG_VERSION=1.21.3
# Wed, 01 Nov 2023 13:54:14 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.3.linux-amd64.tar.gz'; 			sha256='1241381b2843fae5a9707eec1f8fb2ef94d827990582c7c7c32f5bdfbfd420c8'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.3.linux-armv6l.tar.gz'; 			sha256='a1ddcaaf0821a12a800884c14cb4268ce1c1f5a0301e9060646f1e15e611c6c7'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.3.linux-arm64.tar.gz'; 			sha256='fc90fa48ae97ba6368eecb914343590bbb61b388089510d0c56c2dde52987ef3'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.3.linux-386.tar.gz'; 			sha256='fb209fd070db500a84291c5a95251cceeb1723e8f6142de9baca5af70a927c0e'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.3.linux-mips64le.tar.gz'; 			sha256='a569ffbc88b4e14cf2682f65cec950460665e4392b0d78b8868b4718c979bda8'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.3.linux-ppc64le.tar.gz'; 			sha256='3b0e10a3704f164a6e85e0377728ec5fd21524fabe4c925610e34076586d5826'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.3.linux-riscv64.tar.gz'; 			sha256='67d14d3e513e505d1ec3ea34b55641c6c29556603c7899af94045c170c1c0f94'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.3.linux-s390x.tar.gz'; 			sha256='4c78e2e6f4c684a3d5a9bdc97202729053f44eb7be188206f0627ef3e18716b6'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.3.src.tar.gz'; 		sha256='186f2b6f8c8b704e696821b09ab2041a5c1ee13dcbc3156a13adcf75931ee488'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		( 			. /etc/os-release; 			echo "deb https://deb.debian.org/debian $VERSION_CODENAME-backports main" > /etc/apt/sources.list.d/backports.list; 						apt-get update; 			apt-get install -y --no-install-recommends -t "$VERSION_CODENAME-backports" golang-go; 		); 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Wed, 01 Nov 2023 13:54:20 GMT
ENV GOTOOLCHAIN=local
# Wed, 01 Nov 2023 13:54:21 GMT
ENV GOPATH=/go
# Wed, 01 Nov 2023 13:54:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 13:54:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Wed, 01 Nov 2023 13:54:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d002f39ef040587852c73a806a7f49edd2ae7eb78b997c05ca1c5bfedad0506d`  
		Last Modified: Wed, 01 Nov 2023 00:26:33 GMT  
		Size: 58.9 MB (58929494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8932ef1d4dad602784eb2f811c1c987e261b97dfbc072a2c097836198cc588b`  
		Last Modified: Wed, 01 Nov 2023 01:41:47 GMT  
		Size: 16.8 MB (16765480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5598ff1b384ed8a267e359e36806478cf035252da4caca5d70aae48d01bcde`  
		Last Modified: Wed, 01 Nov 2023 01:42:05 GMT  
		Size: 58.9 MB (58865922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11dd01b2b8579928953a47c66d9ad6b5a70e7ece29c98df8fa524a219ab0ca9e`  
		Last Modified: Wed, 01 Nov 2023 14:02:16 GMT  
		Size: 80.5 MB (80542201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691e3dcc2c158a1483c76600bf16675e0a03e096a78d5e771a1ca0fe0039b38b`  
		Last Modified: Wed, 01 Nov 2023 14:02:16 GMT  
		Size: 64.1 MB (64123049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ead9d9afef02ee3765d3d164abced19b6436398b76c86b362f75c30229f0581`  
		Last Modified: Wed, 01 Nov 2023 14:02:03 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bullseye` - linux; s390x

```console
$ docker pull golang@sha256:b7d2ce0206203c0bbecb244476c179c1d837ca248c4d6b90437140dab2131f4a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (254982323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef71f078e196b24c9d261ab3b8b827d990d59d14e3b14b15ca6713e1fa363fb9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Nov 2023 00:42:50 GMT
ADD file:5c168741fe0b80d3b365ae703c082556326a889730963a304b218ab3361d2e8a in / 
# Wed, 01 Nov 2023 00:42:54 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:56:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 01:57:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 12:28:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 12:28:43 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Nov 2023 20:42:44 GMT
ENV GOLANG_VERSION=1.21.4
# Tue, 07 Nov 2023 20:43:03 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.4.linux-amd64.tar.gz'; 			sha256='73cac0215254d0c7d1241fa40837851f3b9a8a742d0b54714cbdfb3feaf8f0af'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.4.linux-armv6l.tar.gz'; 			sha256='6c62e89113750cc77c498194d13a03fadfda22bd2c7d44e8a826fd354db60252'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.4.linux-arm64.tar.gz'; 			sha256='ce1983a7289856c3a918e1fd26d41e072cc39f928adfb11ba1896440849b95da'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.4.linux-386.tar.gz'; 			sha256='64d3e5d295806e137c9e39d1e1f10b00a30fcd5c2f230d72b3298f579bb3c89a'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.4.linux-mips64le.tar.gz'; 			sha256='c7ce3a9dcf03322b79beda474c4a0154393d9029b48f7c2e260fb3365c8a6ad3'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.4.linux-ppc64le.tar.gz'; 			sha256='2c63b36d2adcfb22013102a2ee730f058ec2f93b9f27479793c80b2e3641783f'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.4.linux-riscv64.tar.gz'; 			sha256='9695edd2109544b364daddb32816f5c7980f1f48b8490c51fa2c167f5b2eca48'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.4.linux-s390x.tar.gz'; 			sha256='7a75ba4afc7a96058ca65903d994cd862381825d7dca12b2183f087c757c26c0'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.4.src.tar.gz'; 		sha256='47b26a83d2b65a3c1c1bcace273b69bee49a7a7b5168a7604ded3d26a37bd787'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		( 			. /etc/os-release; 			echo "deb https://deb.debian.org/debian $VERSION_CODENAME-backports main" > /etc/apt/sources.list.d/backports.list; 						apt-get update; 			apt-get install -y --no-install-recommends -t "$VERSION_CODENAME-backports" golang-go; 		); 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Tue, 07 Nov 2023 20:43:08 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Nov 2023 20:43:09 GMT
ENV GOPATH=/go
# Tue, 07 Nov 2023 20:43:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Nov 2023 20:43:09 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Tue, 07 Nov 2023 20:43:09 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a21b3124d41be76bb35d41f49b041980e640c1ea030b4099c4eaa419414f1618`  
		Last Modified: Wed, 01 Nov 2023 00:48:19 GMT  
		Size: 53.3 MB (53296572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb969a0416e6d103d044f625db373b704e7253a5661a213c76711df733f8db0`  
		Last Modified: Wed, 01 Nov 2023 02:06:09 GMT  
		Size: 15.6 MB (15640071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6df2909ff3ad376afb0b5c8415d39aa102919dfc8415cd2c3d3ab0866cb8794`  
		Last Modified: Wed, 01 Nov 2023 02:06:23 GMT  
		Size: 54.1 MB (54065848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d39d8921925b74b4580a8554fb9cbf09dc43e1194a5933035ef5f310c8dd31`  
		Last Modified: Wed, 01 Nov 2023 12:38:14 GMT  
		Size: 65.8 MB (65786756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad13e769aafe8dce94228a2cf14190e52bba07af15324b145162ccd85e10853`  
		Last Modified: Tue, 07 Nov 2023 20:50:24 GMT  
		Size: 66.2 MB (66192920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486ae4587afbc05589c9595efb1532120261e6742e3b01809358f8eaf5b85669`  
		Last Modified: Tue, 07 Nov 2023 20:50:13 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
