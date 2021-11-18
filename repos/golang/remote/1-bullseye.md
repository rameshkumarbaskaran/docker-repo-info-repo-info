## `golang:1-bullseye`

```console
$ docker pull golang@sha256:ed01dea512beaded791a09a3dd31f3e6407ff7b0f68d7e475e8b465f8202abb6
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
$ docker pull golang@sha256:01ade9881e2f3c74662c1915a8b77c2019d4ce0b29b9ea792997de2cdd237cb6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.1 MB (346100411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d9c15f5493bceb5eaa106019ccd14e43fea48ec5c8e7c88df9a0efa55e101b3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:20:30 GMT
ADD file:5259fc086e8295ddbf02e48abef38e9bf93a183079d3631aa7a59306b7f2f9df in / 
# Wed, 17 Nov 2021 02:20:31 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:14:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:14:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Nov 2021 03:14:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 09:51:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 09:51:22 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Nov 2021 09:51:22 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 18 Nov 2021 09:51:43 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.3.linux-amd64.tar.gz'; 			sha256='550f9845451c0c94be679faf116291e7807a8d78b43149f9506c1b15eb89008c'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.3.linux-armv6l.tar.gz'; 			sha256='aa0d5516c8bd61654990916274d27491cfa229d322475502b247a8dc885adec5'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.3.linux-arm64.tar.gz'; 			sha256='06f505c8d27203f78706ad04e47050b49092f1b06dc9ac4fbee4f0e4d015c8d4'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.3.linux-386.tar.gz'; 			sha256='982487a0264626950c635c5e185df68ecaadcca1361956207578d661a7b03bee'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.3.linux-ppc64le.tar.gz'; 			sha256='b821ff58d088c61adc5d7376179a342f325d8715a06abdeb6974f6450663ee60'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.3.linux-s390x.tar.gz'; 			sha256='7d1727e08fef295f48aed2b8124a07e3752e77aea747fcc7aeb8892b8e2f2ad2'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 18 Nov 2021 09:51:44 GMT
ENV GOPATH=/go
# Thu, 18 Nov 2021 09:51:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Nov 2021 09:51:45 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 18 Nov 2021 09:51:46 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:647acf3d48c2780e00cd27bb0984367415f270d78477ef9d5b238e6ebd5290da`  
		Last Modified: Wed, 17 Nov 2021 02:25:17 GMT  
		Size: 54.9 MB (54932774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02967ef003473d9adc6e20868d9d66af85b0871919bcec92419f65c974aa8ce`  
		Last Modified: Wed, 17 Nov 2021 03:23:07 GMT  
		Size: 5.2 MB (5153337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ad2231829e42e6f095971b5d2dc143d97db2d0870571ba4d29ecd599db62cb`  
		Last Modified: Wed, 17 Nov 2021 03:23:07 GMT  
		Size: 10.9 MB (10871856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5576ce26bf1df68da60eeb5162dccde1b69f865d2815aba8b2d29e7181aeb62b`  
		Last Modified: Wed, 17 Nov 2021 03:23:31 GMT  
		Size: 54.6 MB (54566324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9e15b4e149fbbcf4fd5211d571b25bd98c7251db9b0c53490211c6e64e4b86`  
		Last Modified: Thu, 18 Nov 2021 09:55:06 GMT  
		Size: 85.8 MB (85771263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:075916b7332bb2b4dd156a953d0716b184d0a2e5f767f0213fd96238408f766d`  
		Last Modified: Thu, 18 Nov 2021 09:55:14 GMT  
		Size: 134.8 MB (134804702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ac84969409b276b089e47549b6c78e766b04282deceb00989d181ad52056e8`  
		Last Modified: Thu, 18 Nov 2021 09:54:52 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bullseye` - linux; arm variant v5

```console
$ docker pull golang@sha256:ef3b8186e376b4fcbec70eb6cea8b9a84b46f781efb44a1bbc5bc99347c358f1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294534991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4674e1d700da46d2dbd45cad100c2d824ec12d98455cd71dc5b510c4c6728da3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:50:02 GMT
ADD file:48c0196bfa5dfd1137285bf9104248d62f15a734133d8df549f35b6f7989ca19 in / 
# Wed, 17 Nov 2021 02:50:03 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 19:23:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 19:23:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Nov 2021 19:24:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 10:10:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 10:10:39 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Nov 2021 10:10:39 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 18 Nov 2021 10:14:37 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.3.linux-amd64.tar.gz'; 			sha256='550f9845451c0c94be679faf116291e7807a8d78b43149f9506c1b15eb89008c'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.3.linux-armv6l.tar.gz'; 			sha256='aa0d5516c8bd61654990916274d27491cfa229d322475502b247a8dc885adec5'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.3.linux-arm64.tar.gz'; 			sha256='06f505c8d27203f78706ad04e47050b49092f1b06dc9ac4fbee4f0e4d015c8d4'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.3.linux-386.tar.gz'; 			sha256='982487a0264626950c635c5e185df68ecaadcca1361956207578d661a7b03bee'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.3.linux-ppc64le.tar.gz'; 			sha256='b821ff58d088c61adc5d7376179a342f325d8715a06abdeb6974f6450663ee60'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.3.linux-s390x.tar.gz'; 			sha256='7d1727e08fef295f48aed2b8124a07e3752e77aea747fcc7aeb8892b8e2f2ad2'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 18 Nov 2021 10:14:39 GMT
ENV GOPATH=/go
# Thu, 18 Nov 2021 10:14:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Nov 2021 10:14:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 18 Nov 2021 10:14:42 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ce39e946c04dab3f8b463d502d71849e8e6d7291ece7e323f0ec9dac1061af26`  
		Last Modified: Wed, 17 Nov 2021 03:05:19 GMT  
		Size: 52.5 MB (52467904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08bbb4b0e42175293b4f13763886d98a08ea2c365d3bffc892e1f2941ac4438`  
		Last Modified: Wed, 17 Nov 2021 19:43:23 GMT  
		Size: 5.1 MB (5063769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5840619e36fd534698b739a2b185dc0b36b3003c93ec71092d21e1c7670acb2f`  
		Last Modified: Wed, 17 Nov 2021 19:43:26 GMT  
		Size: 10.6 MB (10571101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5da12c4ff6fa069580a2d1ad1ee4ddf02b117cae65e189a6af0c3807af3e151`  
		Last Modified: Wed, 17 Nov 2021 19:44:21 GMT  
		Size: 52.3 MB (52322948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909c9d50da7a5ca3cfcbfa34e022461faaa80af767f94f07504c639a1eedf031`  
		Last Modified: Thu, 18 Nov 2021 10:28:00 GMT  
		Size: 68.7 MB (68705190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45242a1ccd812b0cf563efa68e60b864ba58fe34140f9e94c0bfbb157eab8a47`  
		Last Modified: Thu, 18 Nov 2021 10:28:29 GMT  
		Size: 105.4 MB (105403923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:694a90c17a46535906417fd3998debc003a3ec04c8f1c963ac17092ab69003eb`  
		Last Modified: Thu, 18 Nov 2021 10:27:18 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:cdc4852113d61b3986ee42c581e21b533584b7a07ef6ff027b3f689813717ecf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.4 MB (283399016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4593e0a4b6a29408e1f839161ab4843a24f2bbd99df37829867f80a23993519`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:27:59 GMT
ADD file:d9f40ca54fb79741d1e76c7bca9250f78453d0b39fb6c921337f3071a79a55a9 in / 
# Tue, 12 Oct 2021 01:28:00 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 18:35:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 18:35:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Oct 2021 18:36:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 14 Oct 2021 00:31:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 14 Oct 2021 00:31:36 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:57:59 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 20:58:29 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.3.linux-amd64.tar.gz'; 			sha256='550f9845451c0c94be679faf116291e7807a8d78b43149f9506c1b15eb89008c'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.3.linux-armv6l.tar.gz'; 			sha256='aa0d5516c8bd61654990916274d27491cfa229d322475502b247a8dc885adec5'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.3.linux-arm64.tar.gz'; 			sha256='06f505c8d27203f78706ad04e47050b49092f1b06dc9ac4fbee4f0e4d015c8d4'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.3.linux-386.tar.gz'; 			sha256='982487a0264626950c635c5e185df68ecaadcca1361956207578d661a7b03bee'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.3.linux-ppc64le.tar.gz'; 			sha256='b821ff58d088c61adc5d7376179a342f325d8715a06abdeb6974f6450663ee60'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.3.linux-s390x.tar.gz'; 			sha256='7d1727e08fef295f48aed2b8124a07e3752e77aea747fcc7aeb8892b8e2f2ad2'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 04 Nov 2021 20:58:32 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 20:58:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:58:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 20:58:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:88ce59c3081c4041f41eb407032db40c207cc2d806ba0eb12e170b697db91e52`  
		Last Modified: Tue, 12 Oct 2021 01:43:42 GMT  
		Size: 50.1 MB (50118673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d212c40843ca0a1c4c7b2cd635c4801f93ea3c3470b17d99c403c0e065a8711`  
		Last Modified: Tue, 12 Oct 2021 18:57:54 GMT  
		Size: 4.9 MB (4922722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bdffc4d771520b3975a2a5a85d9d8594ae6d055776a553760db80a5f8e7a279`  
		Last Modified: Tue, 12 Oct 2021 18:57:56 GMT  
		Size: 10.2 MB (10216977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880ea64c0b77d8c40a4101ce92be9b38e5c45e0efe6b4e9c6712d624ba7438be`  
		Last Modified: Tue, 12 Oct 2021 18:58:42 GMT  
		Size: 50.3 MB (50327625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c9ffa78769c2fa52c776a0672a4b8b747baea79cb3d08fd3c9671f8b01ed33c`  
		Last Modified: Thu, 14 Oct 2021 00:41:41 GMT  
		Size: 64.7 MB (64727801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee468a201999a9c098d3d07d77d08b4cd37ea2ddbd232863d27015b92df36a27`  
		Last Modified: Thu, 04 Nov 2021 21:20:03 GMT  
		Size: 103.1 MB (103085062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878d61ffbf5b524c7e89628ca7a0980ffdc06da1dccdf5336a218d98ddd34a6f`  
		Last Modified: Thu, 04 Nov 2021 21:18:56 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:30f9792ddd953426330654948cd1cba3298fa88d0d9598c4659cd99cf8efd672
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.5 MB (307494108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0436fb860e270c75ea0678e36bd0c6accf004c20e49a3fe37cbae69116c7767`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:39:59 GMT
ADD file:eb667e18226da8a1ca5a41beacddc65cd1efec01c3d01e50845c5e89e91ea17c in / 
# Wed, 17 Nov 2021 02:40:00 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 13:26:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 13:26:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Nov 2021 13:27:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 21:43:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 21:43:02 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 21:43:02 GMT
ENV GOLANG_VERSION=1.17.3
# Wed, 17 Nov 2021 21:43:13 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.3.linux-amd64.tar.gz'; 			sha256='550f9845451c0c94be679faf116291e7807a8d78b43149f9506c1b15eb89008c'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.3.linux-armv6l.tar.gz'; 			sha256='aa0d5516c8bd61654990916274d27491cfa229d322475502b247a8dc885adec5'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.3.linux-arm64.tar.gz'; 			sha256='06f505c8d27203f78706ad04e47050b49092f1b06dc9ac4fbee4f0e4d015c8d4'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.3.linux-386.tar.gz'; 			sha256='982487a0264626950c635c5e185df68ecaadcca1361956207578d661a7b03bee'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.3.linux-ppc64le.tar.gz'; 			sha256='b821ff58d088c61adc5d7376179a342f325d8715a06abdeb6974f6450663ee60'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.3.linux-s390x.tar.gz'; 			sha256='7d1727e08fef295f48aed2b8124a07e3752e77aea747fcc7aeb8892b8e2f2ad2'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 17 Nov 2021 21:43:14 GMT
ENV GOPATH=/go
# Wed, 17 Nov 2021 21:43:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 21:43:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 17 Nov 2021 21:43:18 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ce18cd0ba11c2dfa8c1a2d2b325e1e019b14d4ae25ffdeffb0f9686c5496bf5c`  
		Last Modified: Wed, 17 Nov 2021 02:46:45 GMT  
		Size: 53.6 MB (53619024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f138a340a2373acc72dcc4ea9ef08bdf5648aabc5fe08f7e8d25222ca63b7ee`  
		Last Modified: Wed, 17 Nov 2021 13:36:26 GMT  
		Size: 4.9 MB (4937639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34c030205ccb8656e30a58f96bb1edbe7c59bf17f3329ae3c442ec897f2b270`  
		Last Modified: Wed, 17 Nov 2021 13:36:27 GMT  
		Size: 10.7 MB (10655878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d7a1cfcc2070fbe1e702751d85f7074b93d142f6beb03ef66e9ba1c58bcc3e3`  
		Last Modified: Wed, 17 Nov 2021 13:36:49 GMT  
		Size: 54.7 MB (54669696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3944e8986cd8c3c8b139639f790c54f86f4535ab68c1e41236a98d52d7aa28b`  
		Last Modified: Wed, 17 Nov 2021 21:47:55 GMT  
		Size: 81.0 MB (80986958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e186585d8f886e98368df90c4bf765f3c45b8e419c7ef5b9eca493f5202bf7`  
		Last Modified: Wed, 17 Nov 2021 21:47:59 GMT  
		Size: 102.6 MB (102624786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e699867cca8455aab52f7b16d08e0639a4a1e3ca204b28dc32ba2f39e4ca44c1`  
		Last Modified: Wed, 17 Nov 2021 21:47:44 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bullseye` - linux; 386

```console
$ docker pull golang@sha256:f2352094e9d597c21482fa56611ef0ceab0b4b9d0e98b7a989b7a2c009810c2d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.2 MB (321228889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef37fe5005bc134e9a4bd2f48f737eff3f5905cc06688059096185d393103319`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:39:36 GMT
ADD file:b8f9021573a53ec69fa566a396d9a8c68392bd6d659a665c0aea8fbd00164f12 in / 
# Wed, 17 Nov 2021 02:39:37 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 19:24:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 19:24:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Nov 2021 19:24:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 08:19:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 08:19:46 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Nov 2021 08:19:47 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 18 Nov 2021 08:20:19 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.3.linux-amd64.tar.gz'; 			sha256='550f9845451c0c94be679faf116291e7807a8d78b43149f9506c1b15eb89008c'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.3.linux-armv6l.tar.gz'; 			sha256='aa0d5516c8bd61654990916274d27491cfa229d322475502b247a8dc885adec5'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.3.linux-arm64.tar.gz'; 			sha256='06f505c8d27203f78706ad04e47050b49092f1b06dc9ac4fbee4f0e4d015c8d4'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.3.linux-386.tar.gz'; 			sha256='982487a0264626950c635c5e185df68ecaadcca1361956207578d661a7b03bee'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.3.linux-ppc64le.tar.gz'; 			sha256='b821ff58d088c61adc5d7376179a342f325d8715a06abdeb6974f6450663ee60'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.3.linux-s390x.tar.gz'; 			sha256='7d1727e08fef295f48aed2b8124a07e3752e77aea747fcc7aeb8892b8e2f2ad2'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 18 Nov 2021 08:20:20 GMT
ENV GOPATH=/go
# Thu, 18 Nov 2021 08:20:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Nov 2021 08:20:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 18 Nov 2021 08:20:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8d649f3a0e8410b121648ccc552acdac0960691a4da33ff4db9825f9b51ff3f4`  
		Last Modified: Wed, 17 Nov 2021 02:47:12 GMT  
		Size: 55.9 MB (55937586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2d4013b55f8a71bd21767619ba6b97f60534c334cc3dd18176409efe94aa91b`  
		Last Modified: Wed, 17 Nov 2021 19:36:10 GMT  
		Size: 5.3 MB (5283162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f7bc8ea36721b243b9835a80c1c82bd0672cb3c02a2820e0966f9a9a0cf9ed`  
		Last Modified: Wed, 17 Nov 2021 19:36:11 GMT  
		Size: 11.3 MB (11250698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c57b130fe57352c2ebf5bdb1d2ee199402d5390e4e3e9c0457681ffe8a65c6c6`  
		Last Modified: Wed, 17 Nov 2021 19:36:39 GMT  
		Size: 55.9 MB (55917229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced03a0c59fc07ad786dfb5086a06f6e84b9714a55c9e747bf9a161f2924149c`  
		Last Modified: Thu, 18 Nov 2021 08:27:41 GMT  
		Size: 87.2 MB (87222795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b84e0dcb7c834d85493988ae1038c62f36b1b2f021cce1c1ec9235034d6c06cf`  
		Last Modified: Thu, 18 Nov 2021 08:27:45 GMT  
		Size: 105.6 MB (105617264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9a67bf6cf2e36b9098351a36e984a455f60c38f63364e0bc6e8afd8fd66750`  
		Last Modified: Thu, 18 Nov 2021 08:26:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bullseye` - linux; mips64le

```console
$ docker pull golang@sha256:de6f810e7921d0ec31ab0b569c721cfc810601d3ebd9090ef7b7116593c052ec
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.0 MB (291991524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fce00a6050d4fdeead0f8259f0881d62c2e5fc92e249be8532fc63cdee0b81`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Oct 2021 01:10:49 GMT
ADD file:856952232716a2e2d5069387a06a537937a1dec1bb75bc9519c60d6ad226bddb in / 
# Tue, 12 Oct 2021 01:10:50 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 01:49:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 01:49:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Oct 2021 01:50:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 09:33:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 09:33:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:10:24 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 04 Nov 2021 20:20:35 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.3.linux-amd64.tar.gz'; 			sha256='550f9845451c0c94be679faf116291e7807a8d78b43149f9506c1b15eb89008c'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.3.linux-armv6l.tar.gz'; 			sha256='aa0d5516c8bd61654990916274d27491cfa229d322475502b247a8dc885adec5'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.3.linux-arm64.tar.gz'; 			sha256='06f505c8d27203f78706ad04e47050b49092f1b06dc9ac4fbee4f0e4d015c8d4'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.3.linux-386.tar.gz'; 			sha256='982487a0264626950c635c5e185df68ecaadcca1361956207578d661a7b03bee'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.3.linux-ppc64le.tar.gz'; 			sha256='b821ff58d088c61adc5d7376179a342f325d8715a06abdeb6974f6450663ee60'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.3.linux-s390x.tar.gz'; 			sha256='7d1727e08fef295f48aed2b8124a07e3752e77aea747fcc7aeb8892b8e2f2ad2'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 04 Nov 2021 20:20:37 GMT
ENV GOPATH=/go
# Thu, 04 Nov 2021 20:20:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Nov 2021 20:20:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 04 Nov 2021 20:20:40 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3d2cd78b9c44ce4eadbb0cc35b884bfd0dac51123f3c8c6645cb8dc9dc9c1512`  
		Last Modified: Tue, 12 Oct 2021 01:19:18 GMT  
		Size: 53.2 MB (53169836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc92c0f1b1ba16db081439cf0fe0ba300c5acb087b88f97abb47cd8aa1760d6`  
		Last Modified: Tue, 12 Oct 2021 02:04:54 GMT  
		Size: 5.1 MB (5114923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f090a91c9dcffdc8ccb3d0c43f49469a175e0c902bdae900df04c7afe0799f64`  
		Last Modified: Tue, 12 Oct 2021 02:04:56 GMT  
		Size: 10.9 MB (10873345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dca8dc314040adde734540d22d6ece8f751dd2fa78662083691ed36be6a2a8f`  
		Last Modified: Tue, 12 Oct 2021 02:05:49 GMT  
		Size: 53.3 MB (53296535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec238840bc7e9c095c1b03a00718fd1a1712e237dbce38774964c0141fd2a25a`  
		Last Modified: Wed, 13 Oct 2021 10:11:41 GMT  
		Size: 66.9 MB (66896982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7fabae5342647c10c94b5612fd2b663d81746a9a028c53607093c38bd6adf0`  
		Last Modified: Thu, 04 Nov 2021 20:48:43 GMT  
		Size: 102.6 MB (102639777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31bfaac2dfc7582287fb48d2126ed57757fb3825e4e538c21362f4b2dfc27c3b`  
		Last Modified: Thu, 04 Nov 2021 20:47:32 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bullseye` - linux; ppc64le

```console
$ docker pull golang@sha256:475d7bdaf36c224e163c9857ece861799a53dc5112b071c682d666e504832950
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.0 MB (315979087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e681d011cb4218ec3e08487f5057b925a00357550355c75f484818bbb7ff2dd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 03:27:04 GMT
ADD file:85375acb19da58f9eabaa67f8cb425cd1ff2dadb2888bbd9dbfa6223d16fef23 in / 
# Wed, 17 Nov 2021 03:27:20 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 07:40:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 07:40:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Nov 2021 07:42:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 10:38:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 10:38:57 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Nov 2021 10:39:02 GMT
ENV GOLANG_VERSION=1.17.3
# Thu, 18 Nov 2021 10:39:39 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.3.linux-amd64.tar.gz'; 			sha256='550f9845451c0c94be679faf116291e7807a8d78b43149f9506c1b15eb89008c'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.3.linux-armv6l.tar.gz'; 			sha256='aa0d5516c8bd61654990916274d27491cfa229d322475502b247a8dc885adec5'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.3.linux-arm64.tar.gz'; 			sha256='06f505c8d27203f78706ad04e47050b49092f1b06dc9ac4fbee4f0e4d015c8d4'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.3.linux-386.tar.gz'; 			sha256='982487a0264626950c635c5e185df68ecaadcca1361956207578d661a7b03bee'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.3.linux-ppc64le.tar.gz'; 			sha256='b821ff58d088c61adc5d7376179a342f325d8715a06abdeb6974f6450663ee60'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.3.linux-s390x.tar.gz'; 			sha256='7d1727e08fef295f48aed2b8124a07e3752e77aea747fcc7aeb8892b8e2f2ad2'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 18 Nov 2021 10:39:49 GMT
ENV GOPATH=/go
# Thu, 18 Nov 2021 10:39:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Nov 2021 10:39:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 18 Nov 2021 10:40:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ede9cd7c8f1d380c971a130fb3d8a3914bf3a9106702164c23b2cce536fa618c`  
		Last Modified: Wed, 17 Nov 2021 03:52:39 GMT  
		Size: 58.8 MB (58819505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:743814bfd79326104da0238d8edced6b14f63b95734b6dc0e2b7a9d83356b0cb`  
		Last Modified: Wed, 17 Nov 2021 08:25:58 GMT  
		Size: 5.4 MB (5402000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca978d94a6543bbd1c60026602b64e810b4bf65e052dcf19adf2b4d6b518bf8`  
		Last Modified: Wed, 17 Nov 2021 08:25:59 GMT  
		Size: 11.6 MB (11626016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d785f1d8909cb3a3e46844611c28e15781da809be0073e40af017d6e5631d0`  
		Last Modified: Wed, 17 Nov 2021 08:26:57 GMT  
		Size: 58.9 MB (58851458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e1953adba543a4741fa20f91d851f3b2eee62635ec3cd102f45fbe7142b660`  
		Last Modified: Thu, 18 Nov 2021 10:47:06 GMT  
		Size: 80.3 MB (80254657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a091f8553b61595b3931be32344c0f3f91825e4929ed9083a0062050ed3407a`  
		Last Modified: Thu, 18 Nov 2021 10:47:10 GMT  
		Size: 101.0 MB (101025296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9fc77a497a2df6cb2b86a5069c8595bab67b5b63beca23de7bfcbd88cd13b73`  
		Last Modified: Thu, 18 Nov 2021 10:46:51 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bullseye` - linux; s390x

```console
$ docker pull golang@sha256:4ab9c30d8855ae9af12a34c7ac16d9523e5dcee6d3692cec8eb9549530a2c37c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.4 MB (294441099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c3a2c72cf21eccd7ff21601367374ab4b4a137fc517f943b4607c4c1093cc3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:42:07 GMT
ADD file:b7524e775a2033d246d1096765a0eb6eaa5ba6ed6c8b395522579d2c4e7a2e38 in / 
# Wed, 17 Nov 2021 02:42:09 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:07:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:07:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Nov 2021 03:08:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 18:14:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 18:14:32 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 18:14:32 GMT
ENV GOLANG_VERSION=1.17.3
# Wed, 17 Nov 2021 18:14:48 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.3.linux-amd64.tar.gz'; 			sha256='550f9845451c0c94be679faf116291e7807a8d78b43149f9506c1b15eb89008c'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.3.linux-armv6l.tar.gz'; 			sha256='aa0d5516c8bd61654990916274d27491cfa229d322475502b247a8dc885adec5'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.3.linux-arm64.tar.gz'; 			sha256='06f505c8d27203f78706ad04e47050b49092f1b06dc9ac4fbee4f0e4d015c8d4'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.3.linux-386.tar.gz'; 			sha256='982487a0264626950c635c5e185df68ecaadcca1361956207578d661a7b03bee'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.3.linux-ppc64le.tar.gz'; 			sha256='b821ff58d088c61adc5d7376179a342f325d8715a06abdeb6974f6450663ee60'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.3.linux-s390x.tar.gz'; 			sha256='7d1727e08fef295f48aed2b8124a07e3752e77aea747fcc7aeb8892b8e2f2ad2'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 17 Nov 2021 18:14:52 GMT
ENV GOPATH=/go
# Wed, 17 Nov 2021 18:14:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Nov 2021 18:14:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 17 Nov 2021 18:14:53 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ffa47acd07831fbc96680a705da20704bac0016c20dc3c454ecd45cda44b368d`  
		Last Modified: Wed, 17 Nov 2021 02:48:05 GMT  
		Size: 53.2 MB (53207179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c950336719691da019c99e4ff78fe559ab0308ea145757994bdb7be34c6d224`  
		Last Modified: Wed, 17 Nov 2021 03:17:18 GMT  
		Size: 5.1 MB (5137199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d769af2ca44d1c7c206e7190cd71df7cb5ff3df2dd45e1dd52ea447ffb547b1a`  
		Last Modified: Wed, 17 Nov 2021 03:17:19 GMT  
		Size: 10.8 MB (10761499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bbc68017b41a8cc07b10d715e2a23108c5addefa80b01cac1a2ef075bb1acd`  
		Last Modified: Wed, 17 Nov 2021 03:17:36 GMT  
		Size: 54.0 MB (54041155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b3436574e0cc160837d83ea10450a79a77edb52441f24cd8d44db040c079c46`  
		Last Modified: Wed, 17 Nov 2021 18:18:29 GMT  
		Size: 65.5 MB (65502636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50e794ba7a1ff89d1cbbe1bd59967e5c8f03389b5843f077ff37fbecf9cd4e09`  
		Last Modified: Wed, 17 Nov 2021 18:18:33 GMT  
		Size: 105.8 MB (105791275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7dab03cfefb91aeaa06c4c6d45035618fe9bf425d328b34f38ff04329e4b33a`  
		Last Modified: Wed, 17 Nov 2021 18:18:20 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
