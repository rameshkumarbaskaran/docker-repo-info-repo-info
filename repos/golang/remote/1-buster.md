## `golang:1-buster`

```console
$ docker pull golang@sha256:fc58cc5aaeb7fe258a7d31450e8d0480dd2cb07e4c6fd9bf2a09b464ce0e379c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `golang:1-buster` - linux; amd64

```console
$ docker pull golang@sha256:f7a5c5872d4bb68e152be72e4a4bf9a142a47ec2dcbb4074798d4feb6197abd7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.9 MB (317886522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96129f3766cf8b69c32bd0b4be8fbf8f19ef143555b76a7f7b0046ed142e296a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:21:03 GMT
ADD file:1a1eae7a82c66d673971436ce2605e97d107e2934b7cdec876c64923ae6f4f85 in / 
# Wed, 12 May 2021 01:21:03 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:55:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 01:55:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 May 2021 01:56:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 19:23:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 19:23:47 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 May 2021 19:23:47 GMT
ENV GOLANG_VERSION=1.16.4
# Wed, 12 May 2021 19:23:59 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.16.4.linux-amd64.tar.gz'; 			sha256='7154e88f5a8047aad4b80ebace58a059e36e7e2e4eb3b383127a28c711b4ff59'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.16.4.linux-armv6l.tar.gz'; 			sha256='a53391a800ddec749ee90d38992babb27b95cfb864027350c737b9aa8e069494'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.16.4.linux-arm64.tar.gz'; 			sha256='8b18eb05ddda2652d69ab1b1dd1f40dd731799f43c6a58b512ad01ae5b5bba21'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.16.4.linux-386.tar.gz'; 			sha256='cd1b146ef6e9006f27dd99e9687773e7fef30e8c985b7d41bff33e955a3bb53a'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.16.4.linux-ppc64le.tar.gz'; 			sha256='80cfac566e344096a8df8f37bbd21f89e76a6fbe601406565d71a87a665fc125'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.16.4.linux-s390x.tar.gz'; 			sha256='d6431881b3573dc29ecc24fbeab5e5ec25d8c9273aa543769c86a1a3bbac1ddf'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 		sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 12 May 2021 19:24:00 GMT
ENV GOPATH=/go
# Wed, 12 May 2021 19:24:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 May 2021 19:24:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 12 May 2021 19:24:01 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d960726af2bec62a87ceb07182f7b94c47be03909077e23d8226658f80b47f87`  
		Last Modified: Wed, 12 May 2021 01:26:49 GMT  
		Size: 50.4 MB (50433242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8d62473a22dec9ffef056b2017968a9dc484c8f836fb6d79f46980b309e9138`  
		Last Modified: Wed, 12 May 2021 02:04:42 GMT  
		Size: 7.8 MB (7832938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8962bc0fad55b13afedfeb6ad5cb06fd065461cf3e1ae4e7aeae5eeb17b179df`  
		Last Modified: Wed, 12 May 2021 02:04:42 GMT  
		Size: 10.0 MB (9997157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d943ee54c1fa196b54ab9a6673174c66eea04cfa1a4ac5b0328b74f066a4d9`  
		Last Modified: Wed, 12 May 2021 02:05:07 GMT  
		Size: 51.8 MB (51841468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2253e6fbefa9189360a7818eb45effaed9bcb4ff631741a32609b39a2b2c1a2`  
		Last Modified: Wed, 12 May 2021 19:26:13 GMT  
		Size: 68.7 MB (68736689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7fa7c7d5d39b71878fc3f7dfb4faec23a93c7a2f4b23166bb21d0f79a3f5ea`  
		Last Modified: Wed, 12 May 2021 19:26:22 GMT  
		Size: 129.0 MB (129044873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e442f7f89fa3dee035fc1e890d252d32913d08979303d30bf1d8c9470874b2`  
		Last Modified: Wed, 12 May 2021 19:26:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; arm variant v5

```console
$ docker pull golang@sha256:b59d5c680c9f8282de360ccecc84961119332e8378d525734321e8e75e423bc6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269387012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6efd87940b73b045f20f8f371c37128ab21838bd35e5f2dd3027fd37552ed43`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 00:54:57 GMT
ADD file:443be99157e29a4ccb29f5d0ffc9994ce41fb51c512815f76fec9e1fb4d5d8ba in / 
# Wed, 12 May 2021 00:55:00 GMT
CMD ["bash"]
# Thu, 27 May 2021 19:52:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 19:52:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 27 May 2021 19:53:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 20:39:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 20:39:15 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 May 2021 20:39:15 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 27 May 2021 20:43:17 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.16.4.linux-amd64.tar.gz'; 			sha256='7154e88f5a8047aad4b80ebace58a059e36e7e2e4eb3b383127a28c711b4ff59'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.16.4.linux-armv6l.tar.gz'; 			sha256='a53391a800ddec749ee90d38992babb27b95cfb864027350c737b9aa8e069494'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.16.4.linux-arm64.tar.gz'; 			sha256='8b18eb05ddda2652d69ab1b1dd1f40dd731799f43c6a58b512ad01ae5b5bba21'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.16.4.linux-386.tar.gz'; 			sha256='cd1b146ef6e9006f27dd99e9687773e7fef30e8c985b7d41bff33e955a3bb53a'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.16.4.linux-ppc64le.tar.gz'; 			sha256='80cfac566e344096a8df8f37bbd21f89e76a6fbe601406565d71a87a665fc125'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.16.4.linux-s390x.tar.gz'; 			sha256='d6431881b3573dc29ecc24fbeab5e5ec25d8c9273aa543769c86a1a3bbac1ddf'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 		sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 27 May 2021 20:43:18 GMT
ENV GOPATH=/go
# Thu, 27 May 2021 20:43:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 May 2021 20:43:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 27 May 2021 20:43:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:db69af0c9ce605b61ac30d118d6c6ab4f8579b8c80e5469335f2108afa5d2c66`  
		Last Modified: Wed, 12 May 2021 01:09:52 GMT  
		Size: 48.2 MB (48150747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404ba73f5eb1dbb487e50a5cd752625acb36ffba758e241579e2cb88c3becaac`  
		Last Modified: Thu, 27 May 2021 20:04:54 GMT  
		Size: 7.4 MB (7376519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267d6b363679cfa0fcdf5dc9c8564dd9eb369d8d776652cb414b2b23d621ae51`  
		Last Modified: Thu, 27 May 2021 20:04:54 GMT  
		Size: 9.7 MB (9687524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04fed7877fa156e7f1cc5cf959724daf2f0db0041371f88494647de4950b987f`  
		Last Modified: Thu, 27 May 2021 20:05:29 GMT  
		Size: 49.6 MB (49575033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a70a9323ee0082c91dd17ba2104f4c01aa4afde922f472c7fa705c4ef7e098`  
		Last Modified: Thu, 27 May 2021 20:48:39 GMT  
		Size: 52.0 MB (52041787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80312f3d3f44ce0a475af82de49e306bbc83e9134e15657367e3fbc17fbc515e`  
		Last Modified: Thu, 27 May 2021 20:48:52 GMT  
		Size: 102.6 MB (102555247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1496bda31757f08662523a004ea64f69fe479e8c55c5e87d92a3747a6e108d55`  
		Last Modified: Thu, 27 May 2021 20:48:19 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; arm variant v7

```console
$ docker pull golang@sha256:e8b12bc36763aa3ac71150eda38444eb598e3b2e90d383dd72a5e8a56c23ed71
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263243693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97228024917e1a8cd284ccb5bedb3b1cfffe9ff0446a44cb567b4c0fb0f50bbb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:02:10 GMT
ADD file:51a0472692adf18117444dc1f35d6eb3b4d6d672f28a7f6631f9d5d269b0b85d in / 
# Wed, 12 May 2021 01:02:15 GMT
CMD ["bash"]
# Thu, 27 May 2021 00:40:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 00:40:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 27 May 2021 00:40:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 15:05:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 15:05:37 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 May 2021 15:05:37 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 27 May 2021 15:05:54 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.16.4.linux-amd64.tar.gz'; 			sha256='7154e88f5a8047aad4b80ebace58a059e36e7e2e4eb3b383127a28c711b4ff59'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.16.4.linux-armv6l.tar.gz'; 			sha256='a53391a800ddec749ee90d38992babb27b95cfb864027350c737b9aa8e069494'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.16.4.linux-arm64.tar.gz'; 			sha256='8b18eb05ddda2652d69ab1b1dd1f40dd731799f43c6a58b512ad01ae5b5bba21'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.16.4.linux-386.tar.gz'; 			sha256='cd1b146ef6e9006f27dd99e9687773e7fef30e8c985b7d41bff33e955a3bb53a'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.16.4.linux-ppc64le.tar.gz'; 			sha256='80cfac566e344096a8df8f37bbd21f89e76a6fbe601406565d71a87a665fc125'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.16.4.linux-s390x.tar.gz'; 			sha256='d6431881b3573dc29ecc24fbeab5e5ec25d8c9273aa543769c86a1a3bbac1ddf'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 		sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 27 May 2021 15:05:55 GMT
ENV GOPATH=/go
# Thu, 27 May 2021 15:05:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 May 2021 15:05:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 27 May 2021 15:05:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:89475607b1df9fc7eec7efe2fa845738a16cee3e92c1bb864c1f5a93b8303bc6`  
		Last Modified: Wed, 12 May 2021 01:18:49 GMT  
		Size: 45.9 MB (45916922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88447de5eb3eca4a1d96b6980b44d82ac19d121f6b77b826989f8d611fd001b0`  
		Last Modified: Thu, 27 May 2021 01:03:02 GMT  
		Size: 7.1 MB (7124249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25b14665fd0185f2f3b90a8d1825fc8ef9f330e1aea452f60fd70cdcfe99bf4`  
		Last Modified: Thu, 27 May 2021 01:03:02 GMT  
		Size: 9.3 MB (9343721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba65a331625e51ba8f0e1af07dcb97c0583204dda094b5da79672fdf554129c4`  
		Last Modified: Thu, 27 May 2021 01:03:40 GMT  
		Size: 47.4 MB (47356403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28c817b2d28b5d681af2625b1d016403efdb2680145a772baa567b9668da9f0`  
		Last Modified: Thu, 27 May 2021 15:18:15 GMT  
		Size: 53.2 MB (53205162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b89bab7f719221db7063f29b939b035eb6e145aa556a327ea8c2d4a30f30e75`  
		Last Modified: Thu, 27 May 2021 15:18:26 GMT  
		Size: 100.3 MB (100297080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf701d3bdd1ed84c8b9bd5fc2fbec803defe9c46681d45b4fbb00e4aa123e85e`  
		Last Modified: Thu, 27 May 2021 15:18:04 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:5f6481e8bc6f0749586b45b3daa59e7f4937a5bf5a1c2b2a7fb16bc4e9cf4850
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281284248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2401c72858e6a873de141ceb217bb59ae0edd4085aa76e197666a322bca382ce`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 00:50:48 GMT
ADD file:ff9983cd659b3fc32ddfbbdeda76a971afd7d399e6d8b98faea3a9ead0e598f6 in / 
# Wed, 12 May 2021 00:50:52 GMT
CMD ["bash"]
# Thu, 27 May 2021 20:51:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 20:51:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 27 May 2021 20:51:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 22:16:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 22:16:42 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 May 2021 22:16:42 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 27 May 2021 22:16:49 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.16.4.linux-amd64.tar.gz'; 			sha256='7154e88f5a8047aad4b80ebace58a059e36e7e2e4eb3b383127a28c711b4ff59'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.16.4.linux-armv6l.tar.gz'; 			sha256='a53391a800ddec749ee90d38992babb27b95cfb864027350c737b9aa8e069494'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.16.4.linux-arm64.tar.gz'; 			sha256='8b18eb05ddda2652d69ab1b1dd1f40dd731799f43c6a58b512ad01ae5b5bba21'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.16.4.linux-386.tar.gz'; 			sha256='cd1b146ef6e9006f27dd99e9687773e7fef30e8c985b7d41bff33e955a3bb53a'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.16.4.linux-ppc64le.tar.gz'; 			sha256='80cfac566e344096a8df8f37bbd21f89e76a6fbe601406565d71a87a665fc125'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.16.4.linux-s390x.tar.gz'; 			sha256='d6431881b3573dc29ecc24fbeab5e5ec25d8c9273aa543769c86a1a3bbac1ddf'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 		sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 27 May 2021 22:16:50 GMT
ENV GOPATH=/go
# Thu, 27 May 2021 22:16:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 May 2021 22:16:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 27 May 2021 22:16:51 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c54d9402d498e45ed396b5b6fe836f55e4ccadbad745decda3e9f83d880bc677`  
		Last Modified: Wed, 12 May 2021 01:01:40 GMT  
		Size: 49.2 MB (49225351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8aff564b222789ed2823b88e0f1a69ac00cbcbf9349acb8a363d5ef9724182`  
		Last Modified: Thu, 27 May 2021 21:05:15 GMT  
		Size: 7.7 MB (7694906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e893e0778bb86166fb6799aec4e4ac337c4f10172386c8ae9cf3c787331d7d`  
		Last Modified: Thu, 27 May 2021 21:05:15 GMT  
		Size: 10.0 MB (9984325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72bf2dd6193dae84aecaec1d65081288ca49fe0843460035cc060b5aa4e7a9a7`  
		Last Modified: Thu, 27 May 2021 21:05:39 GMT  
		Size: 52.2 MB (52167766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca9f9cb7efb6d58363a4f9dfce73f9ec38c5fce3797d2e1f7c7db156b5d329c`  
		Last Modified: Thu, 27 May 2021 22:25:42 GMT  
		Size: 62.6 MB (62598052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0f3ba017cc6c7b018a9ee48dcfff9f69490997ff184074ad8cae4bea1d3545`  
		Last Modified: Thu, 27 May 2021 22:25:49 GMT  
		Size: 99.6 MB (99613693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d768a4419fe4f566c3a81d7312bd7bf3f9c3ccd9392d90a28a1f870e67e32c51`  
		Last Modified: Thu, 27 May 2021 22:25:32 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; 386

```console
$ docker pull golang@sha256:63121b0615d69f5e14ad1d0e31bfb7ed209ade3ac09d8652509ae25bf95c64b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299664948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c6e1c0397d45de5203c765e2db3712a7391baa6c4da95938b12cd4852492afe`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 00:39:33 GMT
ADD file:f823eb487fd44688b29f866d2c837da27f508db7fc1f19e4dc01dde9ea7c72c4 in / 
# Wed, 12 May 2021 00:39:34 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:09:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 01:09:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 May 2021 01:09:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 17:27:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 17:27:23 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 May 2021 17:27:24 GMT
ENV GOLANG_VERSION=1.16.4
# Wed, 12 May 2021 17:27:37 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.16.4.linux-amd64.tar.gz'; 			sha256='7154e88f5a8047aad4b80ebace58a059e36e7e2e4eb3b383127a28c711b4ff59'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.16.4.linux-armv6l.tar.gz'; 			sha256='a53391a800ddec749ee90d38992babb27b95cfb864027350c737b9aa8e069494'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.16.4.linux-arm64.tar.gz'; 			sha256='8b18eb05ddda2652d69ab1b1dd1f40dd731799f43c6a58b512ad01ae5b5bba21'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.16.4.linux-386.tar.gz'; 			sha256='cd1b146ef6e9006f27dd99e9687773e7fef30e8c985b7d41bff33e955a3bb53a'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.16.4.linux-ppc64le.tar.gz'; 			sha256='80cfac566e344096a8df8f37bbd21f89e76a6fbe601406565d71a87a665fc125'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.16.4.linux-s390x.tar.gz'; 			sha256='d6431881b3573dc29ecc24fbeab5e5ec25d8c9273aa543769c86a1a3bbac1ddf'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 		sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 12 May 2021 17:27:38 GMT
ENV GOPATH=/go
# Wed, 12 May 2021 17:27:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 May 2021 17:27:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 12 May 2021 17:27:40 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:07a4b6b1756691e1f8a89eb64afc18fb9b4a0712eb810679a4b89b1b351f8e9b`  
		Last Modified: Wed, 12 May 2021 00:46:03 GMT  
		Size: 51.2 MB (51200034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb2395b55871bdaf1f7143048f77c63000ab6412664b1ce49fe9a8602e496d1`  
		Last Modified: Wed, 12 May 2021 01:17:52 GMT  
		Size: 8.0 MB (7998534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:106083f164cc6c516cf3c838e5ba0c6870172a26217bd766dac43b0ecc89ca3b`  
		Last Modified: Wed, 12 May 2021 01:17:53 GMT  
		Size: 10.3 MB (10339817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abfd96379aaff5d0e0fbcadade17bc6dd9c9fce6e229d06bbcf028b432ef82d0`  
		Last Modified: Wed, 12 May 2021 01:18:19 GMT  
		Size: 53.4 MB (53438227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba526a5fe4a69af3e8e28c1d228fd8370432cae20f33bf2f0a8f54323d946aee`  
		Last Modified: Wed, 12 May 2021 17:31:15 GMT  
		Size: 73.6 MB (73597884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89380c2081b071f7b538c0eeedff4c511f68025918293bb58959466def7ace5`  
		Last Modified: Wed, 12 May 2021 17:31:20 GMT  
		Size: 103.1 MB (103090298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce7cf8459961f89dbcaa8223357ca681a06c998a5a225b30b979867d8f84ae1`  
		Last Modified: Wed, 12 May 2021 17:30:56 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; mips64le

```console
$ docker pull golang@sha256:9166a0a0bbdd768eea1b71bc62b94101dc2deee5b889e8154c816ca4a25ede72
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.5 MB (271457397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f5cd687c3571064898c7a1d90573888133e465552522ae70b62ee9d380e4576`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:09:17 GMT
ADD file:2e2c1e52b19e85e4299309ed75f088e727e316902a0dd39be198c41ced817b01 in / 
# Wed, 12 May 2021 01:09:18 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:58:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 01:58:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 May 2021 01:59:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 16:09:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 16:09:04 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 May 2021 16:09:04 GMT
ENV GOLANG_VERSION=1.16.4
# Wed, 12 May 2021 16:16:56 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.16.4.linux-amd64.tar.gz'; 			sha256='7154e88f5a8047aad4b80ebace58a059e36e7e2e4eb3b383127a28c711b4ff59'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.16.4.linux-armv6l.tar.gz'; 			sha256='a53391a800ddec749ee90d38992babb27b95cfb864027350c737b9aa8e069494'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.16.4.linux-arm64.tar.gz'; 			sha256='8b18eb05ddda2652d69ab1b1dd1f40dd731799f43c6a58b512ad01ae5b5bba21'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.16.4.linux-386.tar.gz'; 			sha256='cd1b146ef6e9006f27dd99e9687773e7fef30e8c985b7d41bff33e955a3bb53a'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.16.4.linux-ppc64le.tar.gz'; 			sha256='80cfac566e344096a8df8f37bbd21f89e76a6fbe601406565d71a87a665fc125'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.16.4.linux-s390x.tar.gz'; 			sha256='d6431881b3573dc29ecc24fbeab5e5ec25d8c9273aa543769c86a1a3bbac1ddf'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 		sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 12 May 2021 16:16:58 GMT
ENV GOPATH=/go
# Wed, 12 May 2021 16:16:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 May 2021 16:17:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 12 May 2021 16:17:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6e18ab78f0b7ce048045ffb547791aaa698db3869d1da87f71e538a7fd19f965`  
		Last Modified: Wed, 12 May 2021 01:15:53 GMT  
		Size: 49.1 MB (49081826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03651915a251d4aae832ea26b7e72a8d93c3b7bde9b9b309c4069e8de71798fe`  
		Last Modified: Wed, 12 May 2021 02:09:54 GMT  
		Size: 7.3 MB (7252462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc21a03fe417b31a222d86e092660202cc0fae5556a43581e06b7d6a7ae1849`  
		Last Modified: Wed, 12 May 2021 02:09:54 GMT  
		Size: 10.0 MB (10016363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0e8057c7976180c1276687f493d7ba1a8ef256364c51e7c518c539f03b9386`  
		Last Modified: Wed, 12 May 2021 02:10:45 GMT  
		Size: 50.8 MB (50845391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96614d650c8fef4a0dcd461fdcc1c392357450920cb3337b84af6bab0b400b85`  
		Last Modified: Wed, 12 May 2021 16:25:52 GMT  
		Size: 54.7 MB (54651519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b8527fc2cf94ebb0d46ee5382c99e87ea4a4a4fda4443db8f3fbf450398989`  
		Last Modified: Wed, 12 May 2021 16:26:21 GMT  
		Size: 99.6 MB (99609712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1889b9e669fe27da363c12d270bb7252d06a7b94910d5599a545b75ce26de7`  
		Last Modified: Wed, 12 May 2021 16:25:10 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; ppc64le

```console
$ docker pull golang@sha256:db86e3680433584aae1c8744129f0c1f9eee702ac970392666e21459c65dd4c0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.4 MB (302372434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:271148a2be1a6fcf04756cd21cca1cc035819479d019f9b4d6dc2918071360e2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 01:34:15 GMT
ADD file:b714397b44737108500b0256abc9750626cfa28cc0bb52623b9a14bb0e2345fc in / 
# Wed, 12 May 2021 01:34:24 GMT
CMD ["bash"]
# Wed, 12 May 2021 03:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 03:37:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 May 2021 03:42:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 19:14:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 19:14:54 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 May 2021 19:14:59 GMT
ENV GOLANG_VERSION=1.16.4
# Wed, 12 May 2021 19:16:43 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.16.4.linux-amd64.tar.gz'; 			sha256='7154e88f5a8047aad4b80ebace58a059e36e7e2e4eb3b383127a28c711b4ff59'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.16.4.linux-armv6l.tar.gz'; 			sha256='a53391a800ddec749ee90d38992babb27b95cfb864027350c737b9aa8e069494'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.16.4.linux-arm64.tar.gz'; 			sha256='8b18eb05ddda2652d69ab1b1dd1f40dd731799f43c6a58b512ad01ae5b5bba21'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.16.4.linux-386.tar.gz'; 			sha256='cd1b146ef6e9006f27dd99e9687773e7fef30e8c985b7d41bff33e955a3bb53a'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.16.4.linux-ppc64le.tar.gz'; 			sha256='80cfac566e344096a8df8f37bbd21f89e76a6fbe601406565d71a87a665fc125'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.16.4.linux-s390x.tar.gz'; 			sha256='d6431881b3573dc29ecc24fbeab5e5ec25d8c9273aa543769c86a1a3bbac1ddf'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 		sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 12 May 2021 19:16:54 GMT
ENV GOPATH=/go
# Wed, 12 May 2021 19:17:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 May 2021 19:17:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 12 May 2021 19:17:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bd4ac1330adf594df6c60d33ec5060c79833a8455e6cdb9f5ef2be33cb843845`  
		Last Modified: Wed, 12 May 2021 01:43:19 GMT  
		Size: 54.2 MB (54180124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb8ec8ba72b4c906c6a3b88324130a605cfda687a94ed75e901c7cd141492fb`  
		Last Modified: Wed, 12 May 2021 04:19:32 GMT  
		Size: 8.3 MB (8271865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46415d7d07194b30fe4845342dd9c5927deb73698c2cfe9a55c6417b98ed3855`  
		Last Modified: Wed, 12 May 2021 04:19:32 GMT  
		Size: 10.7 MB (10727703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443c274997562dde0054a5cc26e8bbee59190c34ea8b862e917569cfbee85b63`  
		Last Modified: Wed, 12 May 2021 04:20:12 GMT  
		Size: 57.5 MB (57457050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e6cf94b16ff06dc84fad4f21c7aaff73b114a55ee4233bf2ccb9417664dc80`  
		Last Modified: Wed, 12 May 2021 19:21:01 GMT  
		Size: 73.6 MB (73643497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ba384e26d7d49b00b36db2f8ccf4d7e1d9732e8eec9e35082fb368d4ca6ce0`  
		Last Modified: Wed, 12 May 2021 19:21:05 GMT  
		Size: 98.1 MB (98092040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827f6b737f38d5015197d53722d30b6da91ec06781ebddf2f29b12ae155f12d9`  
		Last Modified: Wed, 12 May 2021 19:20:46 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; s390x

```console
$ docker pull golang@sha256:6d8154ee102a1dca51275b36a0b4edd323ed0b9d3316ef6093f6274f798ebcad
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277688615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67632d3398b7632cdf7b2c8ba4dc5a8201ae9579983c1f2ea9e24c52ceedd1b5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 00:43:13 GMT
ADD file:ffd730820ba7e4874e61b094cd8b1b19e272722efa2f96b6c2c0518882aa8010 in / 
# Wed, 12 May 2021 00:43:21 GMT
CMD ["bash"]
# Wed, 12 May 2021 02:24:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 02:24:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 May 2021 02:25:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 16:33:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 16:33:54 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 May 2021 16:33:54 GMT
ENV GOLANG_VERSION=1.16.4
# Wed, 12 May 2021 16:34:29 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.16.4.linux-amd64.tar.gz'; 			sha256='7154e88f5a8047aad4b80ebace58a059e36e7e2e4eb3b383127a28c711b4ff59'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.16.4.linux-armv6l.tar.gz'; 			sha256='a53391a800ddec749ee90d38992babb27b95cfb864027350c737b9aa8e069494'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.16.4.linux-arm64.tar.gz'; 			sha256='8b18eb05ddda2652d69ab1b1dd1f40dd731799f43c6a58b512ad01ae5b5bba21'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.16.4.linux-386.tar.gz'; 			sha256='cd1b146ef6e9006f27dd99e9687773e7fef30e8c985b7d41bff33e955a3bb53a'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.16.4.linux-ppc64le.tar.gz'; 			sha256='80cfac566e344096a8df8f37bbd21f89e76a6fbe601406565d71a87a665fc125'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.16.4.linux-s390x.tar.gz'; 			sha256='d6431881b3573dc29ecc24fbeab5e5ec25d8c9273aa543769c86a1a3bbac1ddf'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 		sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 12 May 2021 16:34:44 GMT
ENV GOPATH=/go
# Wed, 12 May 2021 16:34:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 May 2021 16:34:47 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 12 May 2021 16:34:48 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:03edb521c4b9db23cdd0bda14609ccca13d11f4c37cd9ca16173028e6d3647df`  
		Last Modified: Wed, 12 May 2021 00:47:45 GMT  
		Size: 49.0 MB (49000941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34f82527bf298856cf45773644d350eef4edbbc31c0abda7c268dfbe472c46e`  
		Last Modified: Wed, 12 May 2021 02:34:40 GMT  
		Size: 7.4 MB (7400573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7314687ab69ade4e94423968ff75eb3a6f047e5e53aae12aef126aab10da1d3c`  
		Last Modified: Wed, 12 May 2021 02:34:40 GMT  
		Size: 9.9 MB (9883275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a664f010e5f184251905b6213d5a3762e3d48b827a06000350e3463ea6a1cf53`  
		Last Modified: Wed, 12 May 2021 02:34:56 GMT  
		Size: 51.4 MB (51380390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:569d9f16b7766f9da46f85a3ed93bb64a1e898171e7848be86f3a508c5036e9f`  
		Last Modified: Wed, 12 May 2021 16:37:16 GMT  
		Size: 56.8 MB (56803665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865ed5c569e15cb114993097c7ab7acd31a28689377456bdce44b9ce73514f7f`  
		Last Modified: Wed, 12 May 2021 16:37:24 GMT  
		Size: 103.2 MB (103219614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7767b606ace60e4f2a4dd986715c6bcee199c4cb7ed6cc2bd8820b1e80cba44`  
		Last Modified: Wed, 12 May 2021 16:37:07 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
