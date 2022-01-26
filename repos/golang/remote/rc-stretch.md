## `golang:rc-stretch`

```console
$ docker pull golang@sha256:917614fc1cced898cf4a98319f064f9eef2d531c742ea44752f832edbb1f8775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `golang:rc-stretch` - linux; amd64

```console
$ docker pull golang@sha256:50eb36fca9cf3dac00df32552ea75247872f056eeaf3e87c915781dc238c689f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.7 MB (309739693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb7c15a0fb45f6cb21d62f8a3cb5d1b4bdb454679f2a3948559878067a7a017`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:24:31 GMT
ADD file:4937a62e9e92f367221357a58d7438d1f76546bf3669281431633aebcfd7839d in / 
# Tue, 21 Dec 2021 01:24:31 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:56:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 01:56:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 01:56:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Dec 2021 08:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Dec 2021 08:03:12 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Dec 2021 08:03:12 GMT
ENV GOLANG_VERSION=1.18beta1
# Wed, 22 Dec 2021 08:03:38 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18beta1.linux-amd64.tar.gz'; 			sha256='128f72c5c22640085e4187cd1b540c587cf8fb280f941519bd2d1ae9fdab4f37'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18beta1.linux-armv6l.tar.gz'; 			sha256='d45526c56562abaa473f50302d73abc9f24228108e717a7027024db74fbc774c'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18beta1.linux-arm64.tar.gz'; 			sha256='717092a7265a86af2454cd402b29e8889fb1c83971220fbc37946755e14c891a'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18beta1.linux-386.tar.gz'; 			sha256='1cf671fafb57371615c454d58f8cd78db63682aba0f19350cea80045aa7d2e54'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18beta1.linux-ppc64le.tar.gz'; 			sha256='a0cef27d97197d9e5f3eae3d47b39ea8ab466ee5d97b7ec41335447ec858c47a'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18beta1.linux-s390x.tar.gz'; 			sha256='741749a743d29e7f63f4db64f9e4bc2982b974d254dbb13942d6d3cc4f576194'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18beta1.src.tar.gz'; 		sha256='418c028db14699cb5b2d4907ad3a419d79f789b31916ef8764867e4a78e653a1'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 22 Dec 2021 08:03:39 GMT
ENV GOPATH=/go
# Wed, 22 Dec 2021 08:03:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Dec 2021 08:03:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 22 Dec 2021 08:03:41 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6a56b4def9c45045931a9cf99e9365b558347ae41ec8bfb104a7787e1c3129b0`  
		Last Modified: Tue, 21 Dec 2021 01:31:13 GMT  
		Size: 45.4 MB (45381404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0a7240797a1605f51c11e7c8f49754a8a78c89616dec348fa937886702d115`  
		Last Modified: Tue, 21 Dec 2021 02:04:58 GMT  
		Size: 11.3 MB (11301861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbb8704bdb1f04110dfee1bc6e00f421a37681ff4f136c12337f31c1ccd62bb`  
		Last Modified: Tue, 21 Dec 2021 02:04:58 GMT  
		Size: 4.3 MB (4342385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:737a610bfddaa0e7c87d11580b07707489348ac0fb4cdf2f2265ff2e60246c1b`  
		Last Modified: Tue, 21 Dec 2021 02:05:16 GMT  
		Size: 49.8 MB (49762204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4328e086ba810df9b013c851bb2881cc1fa5bf71974a59e8dc00aad454f796`  
		Last Modified: Wed, 22 Dec 2021 08:08:40 GMT  
		Size: 57.9 MB (57863114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548309df3529e16f41dc1bbe9cacba151f1934d69d79d1f5ed83f723645a1008`  
		Last Modified: Wed, 22 Dec 2021 08:08:52 GMT  
		Size: 141.1 MB (141088569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c33265a58e4e37be5cbe8d3c7624840063ac16d5ae201e986ec1db338ad1864`  
		Last Modified: Wed, 22 Dec 2021 08:08:30 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-stretch` - linux; arm variant v7

```console
$ docker pull golang@sha256:114bc75a2d4da61bc0a39122e3590e47e9885cc78717cdd202750ac823f0e13c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.9 MB (257870524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d45e2b19b4b0a1bc0bbf67f4bc36ee1e7dc3e697aeebe22471a99faefde06f6a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:05:07 GMT
ADD file:60b016ba67df7136a5c9120c3bda872fe6fc9264670eaec4af04649094d2c53d in / 
# Tue, 21 Dec 2021 02:05:08 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:57:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:57:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 02:58:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Dec 2021 16:06:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Dec 2021 16:06:54 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Dec 2021 16:06:54 GMT
ENV GOLANG_VERSION=1.18beta1
# Wed, 22 Dec 2021 16:07:32 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18beta1.linux-amd64.tar.gz'; 			sha256='128f72c5c22640085e4187cd1b540c587cf8fb280f941519bd2d1ae9fdab4f37'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18beta1.linux-armv6l.tar.gz'; 			sha256='d45526c56562abaa473f50302d73abc9f24228108e717a7027024db74fbc774c'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18beta1.linux-arm64.tar.gz'; 			sha256='717092a7265a86af2454cd402b29e8889fb1c83971220fbc37946755e14c891a'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18beta1.linux-386.tar.gz'; 			sha256='1cf671fafb57371615c454d58f8cd78db63682aba0f19350cea80045aa7d2e54'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18beta1.linux-ppc64le.tar.gz'; 			sha256='a0cef27d97197d9e5f3eae3d47b39ea8ab466ee5d97b7ec41335447ec858c47a'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18beta1.linux-s390x.tar.gz'; 			sha256='741749a743d29e7f63f4db64f9e4bc2982b974d254dbb13942d6d3cc4f576194'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18beta1.src.tar.gz'; 		sha256='418c028db14699cb5b2d4907ad3a419d79f789b31916ef8764867e4a78e653a1'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 22 Dec 2021 16:07:34 GMT
ENV GOPATH=/go
# Wed, 22 Dec 2021 16:07:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Dec 2021 16:07:36 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 22 Dec 2021 16:07:36 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1680a7a0944ad84261b1979d7a37cbfaab55a5d7841917a0fb9a78ccc086ee83`  
		Last Modified: Tue, 21 Dec 2021 02:22:04 GMT  
		Size: 42.1 MB (42116934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feceeddac91e698bf009a378cca3bc65e3bee1199adb92912590e31192ac0437`  
		Last Modified: Tue, 21 Dec 2021 03:20:32 GMT  
		Size: 10.0 MB (9956591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee13a902270fb35c27560bff16e80e54c7122abb938b35cc5188ca753ba23cc`  
		Last Modified: Tue, 21 Dec 2021 03:20:29 GMT  
		Size: 3.9 MB (3921249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33cb66d53e7811ef080c8e19ffc98281d9a7e1f083d7f574f6a709b728c2fc01`  
		Last Modified: Tue, 21 Dec 2021 03:21:16 GMT  
		Size: 46.1 MB (46125906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afa3a8aa45ad1434b99db4675b8476a991fd7807914e1b90395c1e84964b9c6`  
		Last Modified: Wed, 22 Dec 2021 16:22:06 GMT  
		Size: 46.2 MB (46193779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df3611d2e49b13a9bea33b0afe7c0ef7be583431f6520c46547ae0c90debf25`  
		Last Modified: Wed, 22 Dec 2021 16:22:52 GMT  
		Size: 109.6 MB (109555910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b3e507a50ce2f0faffd53a576fa041acecc8b23ad2dd895b16bb2cbc4ce0389`  
		Last Modified: Wed, 22 Dec 2021 16:21:41 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-stretch` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:6e74ab239da25da99ed4e6fd29755779a50ade0ada46ff753942738504e7aa1c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.2 MB (262245399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e83a1c873788dcd2268c55894c2f7771305c48b5a83276f2020605c30c42ba`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:44:34 GMT
ADD file:fc57ceb549dcf9223a7806f1dbd83ede31ad1705eda04387f43795b8949b19c4 in / 
# Wed, 26 Jan 2022 01:44:34 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:17:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:17:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 02:18:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 18:47:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 18:48:00 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 18:48:00 GMT
ENV GOLANG_VERSION=1.18beta1
# Wed, 26 Jan 2022 18:49:24 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18beta1.linux-amd64.tar.gz'; 			sha256='128f72c5c22640085e4187cd1b540c587cf8fb280f941519bd2d1ae9fdab4f37'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18beta1.linux-armv6l.tar.gz'; 			sha256='d45526c56562abaa473f50302d73abc9f24228108e717a7027024db74fbc774c'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18beta1.linux-arm64.tar.gz'; 			sha256='717092a7265a86af2454cd402b29e8889fb1c83971220fbc37946755e14c891a'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18beta1.linux-386.tar.gz'; 			sha256='1cf671fafb57371615c454d58f8cd78db63682aba0f19350cea80045aa7d2e54'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18beta1.linux-ppc64le.tar.gz'; 			sha256='a0cef27d97197d9e5f3eae3d47b39ea8ab466ee5d97b7ec41335447ec858c47a'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18beta1.linux-s390x.tar.gz'; 			sha256='741749a743d29e7f63f4db64f9e4bc2982b974d254dbb13942d6d3cc4f576194'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18beta1.src.tar.gz'; 		sha256='418c028db14699cb5b2d4907ad3a419d79f789b31916ef8764867e4a78e653a1'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 26 Jan 2022 18:49:25 GMT
ENV GOPATH=/go
# Wed, 26 Jan 2022 18:49:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Jan 2022 18:49:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 26 Jan 2022 18:49:28 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:11cbe372cf332799e1339b2b8a04723e8224eb56d69212a1308d1df0da55eae2`  
		Last Modified: Wed, 26 Jan 2022 01:52:53 GMT  
		Size: 43.2 MB (43173725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf576a0611a8862b3ac5cc25b79aedd7b2f5a1a457ead352a467fa5b906d0f6`  
		Last Modified: Wed, 26 Jan 2022 02:27:24 GMT  
		Size: 10.2 MB (10216892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc21f7f695aceaf60c5d2590b7acb0d3937aab7af8a9470dd74605632805610`  
		Last Modified: Wed, 26 Jan 2022 02:27:24 GMT  
		Size: 3.9 MB (3873916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16466baa01cbf2b86dbc5f9f876247c80462e423aa7a6b68dfec79de47f85e9e`  
		Last Modified: Wed, 26 Jan 2022 02:27:43 GMT  
		Size: 47.7 MB (47733953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96683053ff7cbf1282b084b86af507f79dfb403dc2a55e375406af0d30cfcd7c`  
		Last Modified: Wed, 26 Jan 2022 19:00:06 GMT  
		Size: 49.0 MB (49022901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94cd7e82b143e1f317923ba00e3e8e082337873294d12417c10f2af84f49a70f`  
		Last Modified: Wed, 26 Jan 2022 19:00:14 GMT  
		Size: 108.2 MB (108223886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289dfd68fb25b9e71e6a4e8495736547e39a850858ff289067c21ef2ee561e17`  
		Last Modified: Wed, 26 Jan 2022 18:59:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-stretch` - linux; 386

```console
$ docker pull golang@sha256:8dcdfa48d9a5605e8d228d1b47e84bc9c1d793441078ab676f8b65ed512a01ed
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.1 MB (288054295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e2f6df4fd8d388d72e93ec01782d94d35d1bd889b270c354585215689619a9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:43:09 GMT
ADD file:55bfa1f20811d5ad7e0824cb8b85e2d7c75ed74ca2784dae41a80c54c2ee3ca8 in / 
# Tue, 21 Dec 2021 01:43:10 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:19:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:19:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 02:20:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Dec 2021 04:16:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Dec 2021 04:16:09 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Dec 2021 04:16:10 GMT
ENV GOLANG_VERSION=1.18beta1
# Wed, 22 Dec 2021 04:16:41 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18beta1.linux-amd64.tar.gz'; 			sha256='128f72c5c22640085e4187cd1b540c587cf8fb280f941519bd2d1ae9fdab4f37'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18beta1.linux-armv6l.tar.gz'; 			sha256='d45526c56562abaa473f50302d73abc9f24228108e717a7027024db74fbc774c'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18beta1.linux-arm64.tar.gz'; 			sha256='717092a7265a86af2454cd402b29e8889fb1c83971220fbc37946755e14c891a'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18beta1.linux-386.tar.gz'; 			sha256='1cf671fafb57371615c454d58f8cd78db63682aba0f19350cea80045aa7d2e54'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18beta1.linux-ppc64le.tar.gz'; 			sha256='a0cef27d97197d9e5f3eae3d47b39ea8ab466ee5d97b7ec41335447ec858c47a'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18beta1.linux-s390x.tar.gz'; 			sha256='741749a743d29e7f63f4db64f9e4bc2982b974d254dbb13942d6d3cc4f576194'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18beta1.src.tar.gz'; 		sha256='418c028db14699cb5b2d4907ad3a419d79f789b31916ef8764867e4a78e653a1'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 22 Dec 2021 04:16:43 GMT
ENV GOPATH=/go
# Wed, 22 Dec 2021 04:16:43 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Dec 2021 04:16:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 22 Dec 2021 04:16:45 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a33597723b77b33e69ce15c675459677dc40eb6b8b822c767d1d106fb2b0365e`  
		Last Modified: Tue, 21 Dec 2021 01:53:18 GMT  
		Size: 46.1 MB (46097707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32c51fce1ac683ec95f0c86c7641f827f198b990803f717ccf546687b4be861`  
		Last Modified: Tue, 21 Dec 2021 02:30:36 GMT  
		Size: 11.4 MB (11359468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8196c269478417443ffdcc48080de94b4136a900f548611f282dc723b34ffa4b`  
		Last Modified: Tue, 21 Dec 2021 02:30:35 GMT  
		Size: 4.6 MB (4564918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0103767f9e30cdb022f48ed2587254717c334195519f35285c473ce97d331f7`  
		Last Modified: Tue, 21 Dec 2021 02:31:01 GMT  
		Size: 51.3 MB (51264824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e10a41c2bb54108fce634a6edb8a6b702cb2c98d81678ad3ee8546ce2ba35ef`  
		Last Modified: Wed, 22 Dec 2021 04:26:03 GMT  
		Size: 62.4 MB (62387753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7618e1a036071e6729f185284e1f8135ff72b1d42351cd2f9d6dd8c4fe763cc`  
		Last Modified: Wed, 22 Dec 2021 04:26:17 GMT  
		Size: 112.4 MB (112379469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49cab24ee97143612b9826aed591cf40e64a752857a60e922d2fca777ec8103b`  
		Last Modified: Wed, 22 Dec 2021 04:25:32 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
