## `golang:buster`

```console
$ docker pull golang@sha256:febccad785b30f1bf980266445fd0afd26df9bf0c6dfcf88c7315a468667f6b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `golang:buster` - linux; amd64

```console
$ docker pull golang@sha256:6d54a51497d4b73e7af3c180b7389c8b0d05a95125069d0f63972d2cf93aac1f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.6 MB (308570610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1072a0788901abf246e0447a8c4d409918a4fc93c8ad129981d448df4d75ca7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 14:54:40 GMT
ADD file:9b7d9295bf7e8307ba4e81ce20770256b964da70dea966568b3515ad026d0b27 in / 
# Fri, 22 Nov 2019 14:54:40 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 00:00:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:00:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 23 Nov 2019 00:01:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 23:05:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Thu, 05 Dec 2019 22:19:41 GMT
ENV GOLANG_VERSION=1.13.5
# Thu, 05 Dec 2019 22:19:53 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='512103d7ad296467814a6e3f635631bd35574cab3369a97a323c9a585ccaa569' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='26259f61d52ee2297b1e8feef3a0fc82144b666a2b95512402c31cc49713c133' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='227b718923e20c846460bbecddde9cb86bad73acc5fb6f8e1a96b81b5c84668b' ;; 		i386) goRelArch='linux-386'; goRelSha256='3b830fa25f79ab08b476f02c84ea4125f41296b074017b492ac1ff748cf1c7c9' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='292814a5ea42a6fc43e1d1ea61c01334e53959e7ab34de86eb5f6efa9742afb6' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='cfbb2959f243880abd1e2efd85d798b8d7ae4a502ab87c4b722c1bd3541e5dc3' ;; 		*) goRelArch='src'; goRelSha256='27d356e2a0b30d9983b60a788cf225da5f914066b37a6b4f69d457ba55a626ff'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Thu, 05 Dec 2019 22:19:53 GMT
ENV GOPATH=/go
# Thu, 05 Dec 2019 22:19:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2019 22:19:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 05 Dec 2019 22:19:54 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:16ea0e8c887910fe167687a0169991b4c1fc165257aab6b116f6a5e61a64e7af`  
		Last Modified: Fri, 22 Nov 2019 15:02:34 GMT  
		Size: 50.4 MB (50379708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50024b0106d53dcbd29889c65bc040439b2bb8947dac16c8c670db894a2c5ba6`  
		Last Modified: Sat, 23 Nov 2019 00:17:22 GMT  
		Size: 7.8 MB (7811508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff95660c69375e19e287b2ea87ca9b4be008cd036e95d541515262b86cc521d9`  
		Last Modified: Sat, 23 Nov 2019 00:17:21 GMT  
		Size: 10.0 MB (9996013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c7d0e5c0bc204b3a36e3f8ff320741da0bd0225e0a67e224c6265c1e208f80a`  
		Last Modified: Sat, 23 Nov 2019 00:17:43 GMT  
		Size: 51.8 MB (51786970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a19d2e6789cf0b5bd768167bbbfd1858b41c6ea6755b3536fd8f0a47accfd5d`  
		Last Modified: Sat, 23 Nov 2019 23:07:45 GMT  
		Size: 68.5 MB (68523665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53b5eb247b8569b06d733e48cedfae42a584f0d2ac7ece5c77906769808e018`  
		Last Modified: Thu, 05 Dec 2019 22:28:50 GMT  
		Size: 120.1 MB (120072620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1e7779aa3cd4e0b39c54bc5a46a5cb8f713f57ed01286bc1d0163efb6f26822`  
		Last Modified: Thu, 05 Dec 2019 22:28:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:buster` - linux; arm variant v7

```console
$ docker pull golang@sha256:a56b787fd5e09f17d2f40635614d87a4797194f17d08e50208dedbb693cc1223
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.9 MB (260877126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:634731c51b0b1534fc6da6f753dbaca37a62c4e72fa973ee262a3568f78b7b0e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 13:22:15 GMT
ADD file:4c51a92fbc511319241c84feac408f0040600ab2230fd8ef007c322f6a5b9532 in / 
# Fri, 22 Nov 2019 13:22:17 GMT
CMD ["bash"]
# Fri, 22 Nov 2019 23:09:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 23:10:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 22 Nov 2019 23:11:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 20:37:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Thu, 05 Dec 2019 22:58:20 GMT
ENV GOLANG_VERSION=1.13.5
# Thu, 05 Dec 2019 22:58:41 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='512103d7ad296467814a6e3f635631bd35574cab3369a97a323c9a585ccaa569' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='26259f61d52ee2297b1e8feef3a0fc82144b666a2b95512402c31cc49713c133' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='227b718923e20c846460bbecddde9cb86bad73acc5fb6f8e1a96b81b5c84668b' ;; 		i386) goRelArch='linux-386'; goRelSha256='3b830fa25f79ab08b476f02c84ea4125f41296b074017b492ac1ff748cf1c7c9' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='292814a5ea42a6fc43e1d1ea61c01334e53959e7ab34de86eb5f6efa9742afb6' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='cfbb2959f243880abd1e2efd85d798b8d7ae4a502ab87c4b722c1bd3541e5dc3' ;; 		*) goRelArch='src'; goRelSha256='27d356e2a0b30d9983b60a788cf225da5f914066b37a6b4f69d457ba55a626ff'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Thu, 05 Dec 2019 22:58:42 GMT
ENV GOPATH=/go
# Thu, 05 Dec 2019 22:58:43 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2019 22:58:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 05 Dec 2019 22:58:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6bac76f7ec397955852a282870ca77ba8bc17beaebffc52bc9053aaa18afc45f`  
		Last Modified: Fri, 22 Nov 2019 13:33:01 GMT  
		Size: 45.9 MB (45859502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43968e81e0eda7d56c4e052a87cd68ef88c023cea38c51a9f30375292f9642d`  
		Last Modified: Fri, 22 Nov 2019 23:30:31 GMT  
		Size: 7.1 MB (7096035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ecba33550822d3a153c6be10451c2d9e738070ee19367ec3136aee9875636ac`  
		Last Modified: Fri, 22 Nov 2019 23:30:31 GMT  
		Size: 9.3 MB (9343198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fffc58cc3ec62e27b8234a554691e44c19d566effa798a9e88bf039d3958d5d6`  
		Last Modified: Fri, 22 Nov 2019 23:30:53 GMT  
		Size: 47.3 MB (47301080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af14c6639beb68a03a1da5e709edc607d67b4af546b08fa0ae7d5eeba8acf02d`  
		Last Modified: Sat, 23 Nov 2019 20:41:00 GMT  
		Size: 53.0 MB (52996835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571cb20e2ac2f0088ee0dd6683530b0fe30ec153bb63f62b80a5b00b4f6b4ac7`  
		Last Modified: Thu, 05 Dec 2019 23:09:24 GMT  
		Size: 98.3 MB (98280320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94164522679430b377f00388d99ae96d79256a04ebd3422bc99bb80d8ed71c68`  
		Last Modified: Thu, 05 Dec 2019 23:08:54 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:buster` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:4a6e32ac1af38afd62442395e287fd26e97f8649cfe4af479cd650f6359ad46f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.9 MB (278934407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:059836fbe26117116848e52db8195e73d6ab81f926c0c1f4d66c78a2cdc32cde`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:40:41 GMT
ADD file:88b3d02fc98aa9138e694bee7d5d1b61b295e4a1c7fae399bf24e52eeff7a5ae in / 
# Sat, 28 Dec 2019 04:40:45 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:04:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 06:05:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 06:05:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sun, 29 Dec 2019 00:19:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Sun, 29 Dec 2019 00:19:59 GMT
ENV GOLANG_VERSION=1.13.5
# Sun, 29 Dec 2019 00:20:19 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='512103d7ad296467814a6e3f635631bd35574cab3369a97a323c9a585ccaa569' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='26259f61d52ee2297b1e8feef3a0fc82144b666a2b95512402c31cc49713c133' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='227b718923e20c846460bbecddde9cb86bad73acc5fb6f8e1a96b81b5c84668b' ;; 		i386) goRelArch='linux-386'; goRelSha256='3b830fa25f79ab08b476f02c84ea4125f41296b074017b492ac1ff748cf1c7c9' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='292814a5ea42a6fc43e1d1ea61c01334e53959e7ab34de86eb5f6efa9742afb6' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='cfbb2959f243880abd1e2efd85d798b8d7ae4a502ab87c4b722c1bd3541e5dc3' ;; 		*) goRelArch='src'; goRelSha256='27d356e2a0b30d9983b60a788cf225da5f914066b37a6b4f69d457ba55a626ff'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Sun, 29 Dec 2019 00:20:21 GMT
ENV GOPATH=/go
# Sun, 29 Dec 2019 00:20:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 29 Dec 2019 00:20:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Sun, 29 Dec 2019 00:20:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:627706d65d1d9b4038d8fd40db52238d4f11d9130a01f23ffae9bf5d41ac5933`  
		Last Modified: Sat, 28 Dec 2019 04:46:38 GMT  
		Size: 49.2 MB (49171876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ac1923ab7a97ecdde2a4f034a8b716d51594ba6fc823c6aaac579c31f51906`  
		Last Modified: Sat, 28 Dec 2019 06:21:16 GMT  
		Size: 7.7 MB (7681148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b000e01546d5b9b3a40a3797f15bc0a1f579786c5ec8da31cbe9502f1927d367`  
		Last Modified: Sat, 28 Dec 2019 06:21:16 GMT  
		Size: 10.0 MB (9983835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8fe6ebd465d85dc79039fbd39712f1fadf5d7ac5fbefe405ef7a4f957a94ce`  
		Last Modified: Sat, 28 Dec 2019 06:21:39 GMT  
		Size: 52.1 MB (52102816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8cbdfdb9424fb643ea7b54950b09c1e0e150d46e21377c399e1a3d01421101c`  
		Last Modified: Sun, 29 Dec 2019 00:23:26 GMT  
		Size: 62.4 MB (62390533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ccaf1330360a4f0f889c847e225f6af96c543106b6e30fb2176231e061f4b5`  
		Last Modified: Sun, 29 Dec 2019 00:24:27 GMT  
		Size: 97.6 MB (97604044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a383edb944750aa293ac59e5030ee9292ba757bd04b0af98667cf78a248d2068`  
		Last Modified: Sun, 29 Dec 2019 00:24:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:buster` - linux; 386

```console
$ docker pull golang@sha256:650c7d505cb9b8faa15c3f9981532c08ebc70a49cd91ec48a159b00d35839bb7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.6 MB (297553836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:391dd865a33fb43c7f26dca0623c08886fa265c722d54d0ffbc1d8ebf811351e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:39:20 GMT
ADD file:c2d3c2cbbc436161afbcdcab7f07d11962ae8a6e99f8ed2c4ff2bcc92455a406 in / 
# Sat, 28 Dec 2019 04:39:21 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 05:21:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:21:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 05:21:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 23:42:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 23:43:22 GMT
ENV GOLANG_VERSION=1.13.5
# Sat, 28 Dec 2019 23:43:37 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='512103d7ad296467814a6e3f635631bd35574cab3369a97a323c9a585ccaa569' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='26259f61d52ee2297b1e8feef3a0fc82144b666a2b95512402c31cc49713c133' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='227b718923e20c846460bbecddde9cb86bad73acc5fb6f8e1a96b81b5c84668b' ;; 		i386) goRelArch='linux-386'; goRelSha256='3b830fa25f79ab08b476f02c84ea4125f41296b074017b492ac1ff748cf1c7c9' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='292814a5ea42a6fc43e1d1ea61c01334e53959e7ab34de86eb5f6efa9742afb6' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='cfbb2959f243880abd1e2efd85d798b8d7ae4a502ab87c4b722c1bd3541e5dc3' ;; 		*) goRelArch='src'; goRelSha256='27d356e2a0b30d9983b60a788cf225da5f914066b37a6b4f69d457ba55a626ff'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Sat, 28 Dec 2019 23:43:37 GMT
ENV GOPATH=/go
# Sat, 28 Dec 2019 23:43:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Dec 2019 23:43:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Sat, 28 Dec 2019 23:43:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b3ff5188aae7f0986a4e7385f8249878f585ef70be99706b3262795514448afc`  
		Last Modified: Sat, 28 Dec 2019 04:44:08 GMT  
		Size: 51.1 MB (51141961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ce66610fca410f78bdf9696c36dad06eb8fef98a4ee82be162c290ea2ce84d`  
		Last Modified: Sat, 28 Dec 2019 05:42:36 GMT  
		Size: 8.0 MB (7981460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231bee61098f24ddd35c94c0c20c114d27580e01b7b1ffe2d17e72a4e07f5c6d`  
		Last Modified: Sat, 28 Dec 2019 05:42:37 GMT  
		Size: 10.3 MB (10338380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6754bbf3b185bf94056033b3f6950dedefaff4d60696107a39dd57a45dd8079`  
		Last Modified: Sat, 28 Dec 2019 05:42:57 GMT  
		Size: 53.4 MB (53380265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c997b3f410c94d19ba97dc1effb638a588457a84c8877bac58e15ea893284621`  
		Last Modified: Sat, 28 Dec 2019 23:46:11 GMT  
		Size: 73.4 MB (73391860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa43c7874f942060002bc1b858bdd2161e302eb8ef2857e044e8b7d839400ead`  
		Last Modified: Sat, 28 Dec 2019 23:46:46 GMT  
		Size: 101.3 MB (101319784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279155d85f2b1cb37f7a07d475f8c178b6a98c8603396569d087d68306e800b3`  
		Last Modified: Sat, 28 Dec 2019 23:46:22 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:buster` - linux; ppc64le

```console
$ docker pull golang@sha256:24428f7a0f168b884ccaa4713fd42a5290bc326cf0d3c577b477c07154e10bd3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300357095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:778d5cdee03761c21f2a6766bd19ed04a2be7188d4a338abea4f1ec1f07f4bd1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Nov 2019 14:54:52 GMT
ADD file:7ea1f6679a4179527d68a59a76ad469bf07b8ce30b1288b4b6437bba9982b896 in / 
# Fri, 22 Nov 2019 14:54:56 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 00:01:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:01:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 23 Nov 2019 00:03:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 16:09:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Thu, 05 Dec 2019 22:17:09 GMT
ENV GOLANG_VERSION=1.13.5
# Thu, 05 Dec 2019 22:17:28 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='512103d7ad296467814a6e3f635631bd35574cab3369a97a323c9a585ccaa569' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='26259f61d52ee2297b1e8feef3a0fc82144b666a2b95512402c31cc49713c133' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='227b718923e20c846460bbecddde9cb86bad73acc5fb6f8e1a96b81b5c84668b' ;; 		i386) goRelArch='linux-386'; goRelSha256='3b830fa25f79ab08b476f02c84ea4125f41296b074017b492ac1ff748cf1c7c9' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='292814a5ea42a6fc43e1d1ea61c01334e53959e7ab34de86eb5f6efa9742afb6' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='cfbb2959f243880abd1e2efd85d798b8d7ae4a502ab87c4b722c1bd3541e5dc3' ;; 		*) goRelArch='src'; goRelSha256='27d356e2a0b30d9983b60a788cf225da5f914066b37a6b4f69d457ba55a626ff'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Thu, 05 Dec 2019 22:17:32 GMT
ENV GOPATH=/go
# Thu, 05 Dec 2019 22:17:36 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2019 22:17:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 05 Dec 2019 22:17:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:127c50d67aec36464937a4593797286304a844c7b8ca8263bbbdd8967229cf5a`  
		Last Modified: Fri, 22 Nov 2019 15:03:30 GMT  
		Size: 54.1 MB (54132225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f59bd6a64d30e2f2a4a62e9589199153ddb61c2f77cc445945b67cd56d87db`  
		Last Modified: Sat, 23 Nov 2019 00:26:54 GMT  
		Size: 8.3 MB (8252166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8328c28b5029be40abe47ebb260b0dab06a48ca9afdbd9a04b1d91fe6480f`  
		Last Modified: Sat, 23 Nov 2019 00:26:53 GMT  
		Size: 10.7 MB (10727041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1a63bd0de74997185aa941953104c26c47babd2334ce4ebc507eefbd72b724`  
		Last Modified: Sat, 23 Nov 2019 00:27:38 GMT  
		Size: 57.4 MB (57400619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601146e6629a3680233cc84e3b9d506cf89914669f04397ee859451cfae73fd2`  
		Last Modified: Sat, 23 Nov 2019 16:15:41 GMT  
		Size: 73.4 MB (73426709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd402e66a375965cad494a5633c81953efc222caf3c70fb16c186cf2aa30979b`  
		Last Modified: Thu, 05 Dec 2019 22:28:23 GMT  
		Size: 96.4 MB (96418180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152f842bb43122e935e6865414e128a61fcaa98d062a42137ab5f6dd430d5e15`  
		Last Modified: Thu, 05 Dec 2019 22:27:35 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:buster` - linux; s390x

```console
$ docker pull golang@sha256:110e6ca357e9cd2d48447176b73136df73cffe23caf802ff547ced06de7099c6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.3 MB (276291354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d687abb358934b9a8e43615e22285d02bb6cf359152ec00a0f23512b3b964b29`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:41:51 GMT
ADD file:aeaf0b11195b2ba7eb7890ce128ad93c114a8e183a516cf2e4ea42da324c57ea in / 
# Sat, 28 Dec 2019 04:41:51 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 05:44:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:45:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 05:45:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 10:49:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 10:50:03 GMT
ENV GOLANG_VERSION=1.13.5
# Sat, 28 Dec 2019 10:50:11 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) goRelArch='linux-amd64'; goRelSha256='512103d7ad296467814a6e3f635631bd35574cab3369a97a323c9a585ccaa569' ;; 		armhf) goRelArch='linux-armv6l'; goRelSha256='26259f61d52ee2297b1e8feef3a0fc82144b666a2b95512402c31cc49713c133' ;; 		arm64) goRelArch='linux-arm64'; goRelSha256='227b718923e20c846460bbecddde9cb86bad73acc5fb6f8e1a96b81b5c84668b' ;; 		i386) goRelArch='linux-386'; goRelSha256='3b830fa25f79ab08b476f02c84ea4125f41296b074017b492ac1ff748cf1c7c9' ;; 		ppc64el) goRelArch='linux-ppc64le'; goRelSha256='292814a5ea42a6fc43e1d1ea61c01334e53959e7ab34de86eb5f6efa9742afb6' ;; 		s390x) goRelArch='linux-s390x'; goRelSha256='cfbb2959f243880abd1e2efd85d798b8d7ae4a502ab87c4b722c1bd3541e5dc3' ;; 		*) goRelArch='src'; goRelSha256='27d356e2a0b30d9983b60a788cf225da5f914066b37a6b4f69d457ba55a626ff'; 			echo >&2; echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; echo >&2 ;; 	esac; 		url="https://golang.org/dl/go${GOLANG_VERSION}.${goRelArch}.tar.gz"; 	wget -O go.tgz "$url"; 	echo "${goRelSha256} *go.tgz" | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ "$goRelArch" = 'src' ]; then 		echo >&2; 		echo >&2 'error: UNIMPLEMENTED'; 		echo >&2 'TODO install golang-any from jessie-backports for GOROOT_BOOTSTRAP (and uninstall after build)'; 		echo >&2; 		exit 1; 	fi; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Sat, 28 Dec 2019 10:50:12 GMT
ENV GOPATH=/go
# Sat, 28 Dec 2019 10:50:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Dec 2019 10:50:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Sat, 28 Dec 2019 10:50:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3596c5a237f76c32832c1879a3d0c763989cb13fac0024673b03e9b549b868ea`  
		Last Modified: Sat, 28 Dec 2019 04:44:54 GMT  
		Size: 49.0 MB (48954508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a87e4c2949f278ec7636f6762169d70bd2588ed301cc3e2721aa830a9227fc`  
		Last Modified: Sat, 28 Dec 2019 05:53:25 GMT  
		Size: 7.4 MB (7380503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33b91142ed28640cd70826a84025844f0fa1e7bc50f10b67f6ee03ed2f013ae`  
		Last Modified: Sat, 28 Dec 2019 05:53:25 GMT  
		Size: 9.9 MB (9880177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23386745bcbf27928754e130693faba015951a5923f1fcf54478337f15c7e06`  
		Last Modified: Sat, 28 Dec 2019 05:53:39 GMT  
		Size: 51.3 MB (51318842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0fbfcf3c9c79e6865a1fef5477d5d13f0ab68756fce199e5bcddd2c8d98e57`  
		Last Modified: Sat, 28 Dec 2019 10:52:07 GMT  
		Size: 56.6 MB (56590901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69faab8d5a3abf62332158ac5fc62c46ab9f4e3dfc3bc3066d6d3352372643f5`  
		Last Modified: Sat, 28 Dec 2019 10:52:30 GMT  
		Size: 102.2 MB (102166297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef5966ea04196dfc39d2438a417747bb18e3b2017a53b3e183881cbda60d07f2`  
		Last Modified: Sat, 28 Dec 2019 10:52:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
