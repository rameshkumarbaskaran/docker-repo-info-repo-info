## `golang:bullseye`

```console
$ docker pull golang@sha256:8b9971c37678d2c4c04e7dd4e430baec049647d72ed97bf5e6a41ef8e77e74a5
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

### `golang:bullseye` - linux; amd64

```console
$ docker pull golang@sha256:2fddf0539591f8e364c9adb3d495d1ba2ca8a8df420ad23b58e7bcee7986ea6c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.5 MB (360527506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce494d5814b5644d6ab2321aa466ef7a3c54ba46141b1efce6184fb7c63d360`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:42 GMT
ADD file:26702ba2c3e94cb21cdb3c550cf01cf848823d160f3417b559116d4c718e5df0 in / 
# Tue, 25 Oct 2022 01:43:42 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 09:23:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 09:23:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 09:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 00:48:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 00:48:52 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Oct 2022 00:48:52 GMT
ENV GOLANG_VERSION=1.19.2
# Wed, 26 Oct 2022 00:49:06 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.19.2.linux-amd64.tar.gz'; 			sha256='5e8c5a74fe6470dd7e055a461acda8bb4050ead8c2df70f227e3ff7d8eb7eeb6'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.19.2.linux-armv6l.tar.gz'; 			sha256='f3ccec7816ecd704ebafd130b08b8ad97c55402a8193a107b63e9de12ab90118'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.19.2.linux-arm64.tar.gz'; 			sha256='b62a8d9654436c67c14a0c91e931d50440541f09eb991a987536cb982903126d'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.19.2.linux-386.tar.gz'; 			sha256='ba8c97965e0856c69c9ca2c86f96bec5bb21de43e6533e25494bb211d85cda1b'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.19.2.linux-ppc64le.tar.gz'; 			sha256='37e1d4342f7103aeb9babeabe8c71ef3dba23db28db525071119e94b2aa21d7d'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.19.2.linux-s390x.tar.gz'; 			sha256='51b45dec41295215df17f78e67d1a373b9dda97a5e539bed440974da5ffc97de'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.2.src.tar.gz'; 		sha256='2ce930d70a931de660fdaf271d70192793b1b240272645bf0275779f6704df6b'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Wed, 26 Oct 2022 00:49:07 GMT
ENV GOPATH=/go
# Wed, 26 Oct 2022 00:49:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Oct 2022 00:49:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 26 Oct 2022 00:49:08 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:17c9e6141fdb3387e5a1c07d4f9b6a05ac1498e96029fa3ea55470d4504f7770`  
		Last Modified: Tue, 25 Oct 2022 01:47:28 GMT  
		Size: 55.0 MB (55046332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4a4c6caea8801bb0b7377e10220a914da403bc93fa79663cbf2dcf1800b6f1`  
		Last Modified: Tue, 25 Oct 2022 09:47:36 GMT  
		Size: 5.2 MB (5164775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4edced8587e6c18412817019074f5e04a8ede4e2fc89d06af13df3f80d78a70d`  
		Last Modified: Tue, 25 Oct 2022 09:47:36 GMT  
		Size: 10.9 MB (10877322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7969cffbf46e6a91291fd76b19ecbe93c03ea4ded0d14042aecb4c0c4211a43`  
		Last Modified: Tue, 25 Oct 2022 09:47:56 GMT  
		Size: 54.6 MB (54586464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa7548a174d51c2cadd24f9e629f436fbf1f501daba3e757d78c32f31c7fe83`  
		Last Modified: Wed, 26 Oct 2022 00:51:23 GMT  
		Size: 86.0 MB (85968442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a86067690e454a7f294329b6cc83502da1e3748726c0f1819d37f6dd3a69884c`  
		Last Modified: Wed, 26 Oct 2022 00:51:33 GMT  
		Size: 148.9 MB (148884015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a75b47d9366434d29afda0a459a52f8c199b1150e2343fcbe727d87648afb5`  
		Last Modified: Wed, 26 Oct 2022 00:51:10 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:bullseye` - linux; arm variant v5

```console
$ docker pull golang@sha256:556a8d55aee993b75d32dea3a4facd6b4357642c82e89cc57f2e63788550885e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.6 MB (308609786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b227b44e277ac58c0f0ab1e83630c92f67a6fa65fa1d773924a8fba6e9086f75`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:06:19 GMT
ADD file:b314b98654e8532fd10a08a172ea5c3edb7d7a36c7faf85d06d14be12f7b83ef in / 
# Tue, 25 Oct 2022 03:06:19 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:12:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:12:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 06:12:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 14:57:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 14:57:03 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Oct 2022 14:57:03 GMT
ENV GOLANG_VERSION=1.19.2
# Tue, 25 Oct 2022 14:59:18 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.19.2.linux-amd64.tar.gz'; 			sha256='5e8c5a74fe6470dd7e055a461acda8bb4050ead8c2df70f227e3ff7d8eb7eeb6'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.19.2.linux-armv6l.tar.gz'; 			sha256='f3ccec7816ecd704ebafd130b08b8ad97c55402a8193a107b63e9de12ab90118'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.19.2.linux-arm64.tar.gz'; 			sha256='b62a8d9654436c67c14a0c91e931d50440541f09eb991a987536cb982903126d'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.19.2.linux-386.tar.gz'; 			sha256='ba8c97965e0856c69c9ca2c86f96bec5bb21de43e6533e25494bb211d85cda1b'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.19.2.linux-ppc64le.tar.gz'; 			sha256='37e1d4342f7103aeb9babeabe8c71ef3dba23db28db525071119e94b2aa21d7d'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.19.2.linux-s390x.tar.gz'; 			sha256='51b45dec41295215df17f78e67d1a373b9dda97a5e539bed440974da5ffc97de'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.2.src.tar.gz'; 		sha256='2ce930d70a931de660fdaf271d70192793b1b240272645bf0275779f6704df6b'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Tue, 25 Oct 2022 14:59:19 GMT
ENV GOPATH=/go
# Tue, 25 Oct 2022 14:59:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Oct 2022 14:59:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 25 Oct 2022 14:59:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1f0ecb08923b99bef3f82c2e88603bb53e3ed084c13252275c05039cc279c158`  
		Last Modified: Tue, 25 Oct 2022 03:11:15 GMT  
		Size: 52.5 MB (52547473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b399c5eb53b4c35fa33682a82d73bdc4b096cd78ae95fe36c4ed81d18f6849`  
		Last Modified: Tue, 25 Oct 2022 06:19:02 GMT  
		Size: 5.1 MB (5072235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ccdd06393cd3873a3cc8b9cbe170a2032fd61d1d545b7045b649faf2f4e732`  
		Last Modified: Tue, 25 Oct 2022 06:19:02 GMT  
		Size: 10.6 MB (10574279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aafe0e287af4e488dcda51195e4eb1ae1386e3265989c457172f32f6357bf26`  
		Last Modified: Tue, 25 Oct 2022 06:19:28 GMT  
		Size: 52.3 MB (52322157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd12d31bb97d2b018145d62602ea169f8eb5890a0c9990ed30115297d7b0331`  
		Last Modified: Tue, 25 Oct 2022 15:02:28 GMT  
		Size: 68.9 MB (68865696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3c8d1f2ad9c907637c58edeb997667b5b8a29f10e34c889a23a9e5a4b7dff3`  
		Last Modified: Tue, 25 Oct 2022 15:02:38 GMT  
		Size: 119.2 MB (119227820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb6c0365e682c850c38225033c41a0403ed8ff4bd41cf664663c817bcf3a2484`  
		Last Modified: Tue, 25 Oct 2022 15:02:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:22c5ee0a984fd98a27cd63cde8d04d5300dee153c8086abc476ba86ca43e4511
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.3 MB (297316650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b6860fc75cf5714a6fa79309af8667e3e61ea8569cbad64e6a3520ab92036d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:14:06 GMT
ADD file:94d6b607b174c11c18753fac156b0ca5ecda941da3d456e136b8b14457810d37 in / 
# Tue, 25 Oct 2022 03:14:06 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 04:36:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 04:36:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Oct 2022 04:36:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 27 Oct 2022 03:10:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 27 Oct 2022 03:10:03 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Oct 2022 03:10:03 GMT
ENV GOLANG_VERSION=1.19.2
# Thu, 27 Oct 2022 03:10:21 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.19.2.linux-amd64.tar.gz'; 			sha256='5e8c5a74fe6470dd7e055a461acda8bb4050ead8c2df70f227e3ff7d8eb7eeb6'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.19.2.linux-armv6l.tar.gz'; 			sha256='f3ccec7816ecd704ebafd130b08b8ad97c55402a8193a107b63e9de12ab90118'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.19.2.linux-arm64.tar.gz'; 			sha256='b62a8d9654436c67c14a0c91e931d50440541f09eb991a987536cb982903126d'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.19.2.linux-386.tar.gz'; 			sha256='ba8c97965e0856c69c9ca2c86f96bec5bb21de43e6533e25494bb211d85cda1b'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.19.2.linux-ppc64le.tar.gz'; 			sha256='37e1d4342f7103aeb9babeabe8c71ef3dba23db28db525071119e94b2aa21d7d'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.19.2.linux-s390x.tar.gz'; 			sha256='51b45dec41295215df17f78e67d1a373b9dda97a5e539bed440974da5ffc97de'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.2.src.tar.gz'; 		sha256='2ce930d70a931de660fdaf271d70192793b1b240272645bf0275779f6704df6b'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Thu, 27 Oct 2022 03:10:23 GMT
ENV GOPATH=/go
# Thu, 27 Oct 2022 03:10:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Oct 2022 03:10:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 27 Oct 2022 03:10:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a9bec1cbb822a75428a679c01f232b1af10cce0bdc1bf6507d26e8d79ad54300`  
		Last Modified: Tue, 25 Oct 2022 03:20:41 GMT  
		Size: 50.2 MB (50209987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9e47cd2446328779ff30de254793eaf539fec260638990e7d8dd3d29342fca`  
		Last Modified: Wed, 26 Oct 2022 05:10:38 GMT  
		Size: 4.9 MB (4932764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8deb44fa055f393de7346c484ab2ff3ef90e7efc4ebb018f932b377361e3b45`  
		Last Modified: Wed, 26 Oct 2022 05:10:38 GMT  
		Size: 10.2 MB (10218474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e22aca21bac1ccd293dcbdab0f501e5f245365480a29e4d11572ddc5092e2287`  
		Last Modified: Wed, 26 Oct 2022 05:11:04 GMT  
		Size: 50.3 MB (50345195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67f5be6f3d2ed5848e4dcc85b6d7f27282473847177c2271047663070fe09a36`  
		Last Modified: Thu, 27 Oct 2022 03:22:18 GMT  
		Size: 64.9 MB (64890965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0cc86958819942d76f1451dda014d3347d4d686f9b49df7d0f38383422b7953`  
		Last Modified: Thu, 27 Oct 2022 03:22:29 GMT  
		Size: 116.7 MB (116719140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b716b87ce4fa303e20ce2c75af85d2c1e338103acf568c800f93e7d0d890b2`  
		Last Modified: Thu, 27 Oct 2022 03:22:07 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:e747d62bf5ae59326b90d95899413cbc239e98c7932c90a9d6368f6e44109236
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320896277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b87b32e8389cfe7d8291583b950c0d2c0b98509b9a91bc0998c477706f0d03`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:45:55 GMT
ADD file:b16745ece8ef84c028d7e9ac4bf026ac64f885d4170bfcc9d435f237144a1b99 in / 
# Tue, 25 Oct 2022 05:45:56 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:58:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:58:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 07:59:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 08:09:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 08:09:13 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Oct 2022 08:09:13 GMT
ENV GOLANG_VERSION=1.19.2
# Wed, 26 Oct 2022 08:09:22 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.19.2.linux-amd64.tar.gz'; 			sha256='5e8c5a74fe6470dd7e055a461acda8bb4050ead8c2df70f227e3ff7d8eb7eeb6'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.19.2.linux-armv6l.tar.gz'; 			sha256='f3ccec7816ecd704ebafd130b08b8ad97c55402a8193a107b63e9de12ab90118'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.19.2.linux-arm64.tar.gz'; 			sha256='b62a8d9654436c67c14a0c91e931d50440541f09eb991a987536cb982903126d'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.19.2.linux-386.tar.gz'; 			sha256='ba8c97965e0856c69c9ca2c86f96bec5bb21de43e6533e25494bb211d85cda1b'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.19.2.linux-ppc64le.tar.gz'; 			sha256='37e1d4342f7103aeb9babeabe8c71ef3dba23db28db525071119e94b2aa21d7d'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.19.2.linux-s390x.tar.gz'; 			sha256='51b45dec41295215df17f78e67d1a373b9dda97a5e539bed440974da5ffc97de'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.2.src.tar.gz'; 		sha256='2ce930d70a931de660fdaf271d70192793b1b240272645bf0275779f6704df6b'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Wed, 26 Oct 2022 08:09:25 GMT
ENV GOPATH=/go
# Wed, 26 Oct 2022 08:09:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Oct 2022 08:09:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 26 Oct 2022 08:09:25 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8e1d92e7d04d2a9a9880cb45dc3c32c2805912cd86abed96d0ada3ff28748205`  
		Last Modified: Tue, 25 Oct 2022 05:48:40 GMT  
		Size: 53.7 MB (53701966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66eadbf427bb41b3e329a95935c65b09c6d3b7a9c2fa8e08417e497df02ed996`  
		Last Modified: Tue, 25 Oct 2022 08:30:22 GMT  
		Size: 5.2 MB (5151506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9731f4e3bc3680179c10cece663cf0cfe0488918d6795406f4b76f07b787de`  
		Last Modified: Tue, 25 Oct 2022 08:30:22 GMT  
		Size: 10.9 MB (10874174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d337cb12fd7c6fe341850cd38e880f1806d49a65832c9804b06d00f9032382e0`  
		Last Modified: Tue, 25 Oct 2022 08:30:42 GMT  
		Size: 54.7 MB (54683990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a70e778606f888a21badcd0a0dae68201b78b263e5bbc2532ee92e286646f7de`  
		Last Modified: Wed, 26 Oct 2022 08:16:29 GMT  
		Size: 81.4 MB (81371367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eebbd0de1400e890feac0b4b2a34feca7d973f3393e85f94ba9df03d72e12e02`  
		Last Modified: Wed, 26 Oct 2022 08:16:33 GMT  
		Size: 115.1 MB (115113120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee96d99957b7576c05df0b5163cecbee865a5b9e7e6f1360e14405b78e397c3`  
		Last Modified: Wed, 26 Oct 2022 08:16:20 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:bullseye` - linux; 386

```console
$ docker pull golang@sha256:83e17fa6ed971330c1c59310b14b048cad365af19a78aaca919781302077a2b3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.3 MB (335259050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c6c590ddb899dc14ca810d2098678af17c9cc0f45d8a4e07bbd782bf76024a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 02:22:19 GMT
ADD file:aa26f69b37c3e144d08e17bb9be7302ec89ae0579121c874a35f336d7077fd3b in / 
# Tue, 25 Oct 2022 02:22:19 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 05:15:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 05:15:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 05:15:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 18:22:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 18:22:42 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Oct 2022 18:22:43 GMT
ENV GOLANG_VERSION=1.19.2
# Tue, 25 Oct 2022 18:22:58 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.19.2.linux-amd64.tar.gz'; 			sha256='5e8c5a74fe6470dd7e055a461acda8bb4050ead8c2df70f227e3ff7d8eb7eeb6'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.19.2.linux-armv6l.tar.gz'; 			sha256='f3ccec7816ecd704ebafd130b08b8ad97c55402a8193a107b63e9de12ab90118'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.19.2.linux-arm64.tar.gz'; 			sha256='b62a8d9654436c67c14a0c91e931d50440541f09eb991a987536cb982903126d'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.19.2.linux-386.tar.gz'; 			sha256='ba8c97965e0856c69c9ca2c86f96bec5bb21de43e6533e25494bb211d85cda1b'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.19.2.linux-ppc64le.tar.gz'; 			sha256='37e1d4342f7103aeb9babeabe8c71ef3dba23db28db525071119e94b2aa21d7d'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.19.2.linux-s390x.tar.gz'; 			sha256='51b45dec41295215df17f78e67d1a373b9dda97a5e539bed440974da5ffc97de'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.2.src.tar.gz'; 		sha256='2ce930d70a931de660fdaf271d70192793b1b240272645bf0275779f6704df6b'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Tue, 25 Oct 2022 18:22:59 GMT
ENV GOPATH=/go
# Tue, 25 Oct 2022 18:23:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Oct 2022 18:23:01 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 25 Oct 2022 18:23:02 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8caf426a2703f99fb0be4b03411ecaa580d102f7c47ef43b422b6d7c13c380e2`  
		Last Modified: Tue, 25 Oct 2022 02:27:54 GMT  
		Size: 56.0 MB (56023960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b92a2ff5c72653a0679aa7f5e2bc695011c0a71faa424229e560957d204dab`  
		Last Modified: Tue, 25 Oct 2022 05:27:37 GMT  
		Size: 5.1 MB (5086887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c6856a3002e686ceb6d48d078731366f576ed3adcb73bd49dcb300057732904`  
		Last Modified: Tue, 25 Oct 2022 05:27:38 GMT  
		Size: 11.0 MB (11032526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e88080d3b5ba1edc8623a97d068bd040dfb89f2bc7bdfc0984d11fc35ff5885`  
		Last Modified: Tue, 25 Oct 2022 05:28:00 GMT  
		Size: 55.9 MB (55924404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:257d1a174521bbc2317acbc6ba9f9a91cb963244f0794bd1196e33e7ce794e4b`  
		Last Modified: Tue, 25 Oct 2022 18:26:25 GMT  
		Size: 87.2 MB (87163943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0ff5c817c1d9c561b6e9d49685b4a6a83b226ad36cace46843c7e656581f42`  
		Last Modified: Tue, 25 Oct 2022 18:26:29 GMT  
		Size: 120.0 MB (120027205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58e259531da00c88ab16b45e4c4926c52fbed090c9257880762aa18812a09830`  
		Last Modified: Tue, 25 Oct 2022 18:26:12 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:bullseye` - linux; mips64le

```console
$ docker pull golang@sha256:ab379bfc96c98b559b3628597ac6c6a1395cd54b71dfb073c964e2d53d41d8da
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.0 MB (304000951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97db8a9a667dcfa29c1083f7b960f796afd05c0eca5f65d65d804ebfc3504166`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 04:38:51 GMT
ADD file:617ca04150550c7e3a178e3ac85bb359b17a390090ce6ce72a6f2ed1db10ab63 in / 
# Tue, 25 Oct 2022 04:38:57 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 09:30:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 09:31:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 09:33:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 11:51:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 11:51:37 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Oct 2022 11:51:41 GMT
ENV GOLANG_VERSION=1.19.2
# Wed, 26 Oct 2022 12:04:01 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.19.2.linux-amd64.tar.gz'; 			sha256='5e8c5a74fe6470dd7e055a461acda8bb4050ead8c2df70f227e3ff7d8eb7eeb6'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.19.2.linux-armv6l.tar.gz'; 			sha256='f3ccec7816ecd704ebafd130b08b8ad97c55402a8193a107b63e9de12ab90118'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.19.2.linux-arm64.tar.gz'; 			sha256='b62a8d9654436c67c14a0c91e931d50440541f09eb991a987536cb982903126d'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.19.2.linux-386.tar.gz'; 			sha256='ba8c97965e0856c69c9ca2c86f96bec5bb21de43e6533e25494bb211d85cda1b'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.19.2.linux-ppc64le.tar.gz'; 			sha256='37e1d4342f7103aeb9babeabe8c71ef3dba23db28db525071119e94b2aa21d7d'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.19.2.linux-s390x.tar.gz'; 			sha256='51b45dec41295215df17f78e67d1a373b9dda97a5e539bed440974da5ffc97de'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.2.src.tar.gz'; 		sha256='2ce930d70a931de660fdaf271d70192793b1b240272645bf0275779f6704df6b'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Wed, 26 Oct 2022 12:04:09 GMT
ENV GOPATH=/go
# Wed, 26 Oct 2022 12:04:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Oct 2022 12:04:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 26 Oct 2022 12:04:30 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e3c84cb4c321de8db072180e3509c5bbcf8e562ff11c03241bdf082184fe74d6`  
		Last Modified: Tue, 25 Oct 2022 04:46:42 GMT  
		Size: 53.3 MB (53265848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3db3e162cf97fdacf5ea7f9f3912781648668e28872229f94c59a0ede7eb374`  
		Last Modified: Tue, 25 Oct 2022 09:51:57 GMT  
		Size: 4.9 MB (4919493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb2f56957fe9f71a2e7c596a334686320ab2569f1a54e243bfcd3f42ebae17c`  
		Last Modified: Tue, 25 Oct 2022 09:51:59 GMT  
		Size: 10.7 MB (10661828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57a581172d92713c67937b8552f2518b0661de8146176b186886f6dd01ea188`  
		Last Modified: Tue, 25 Oct 2022 09:52:48 GMT  
		Size: 53.3 MB (53306457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a848178ef525ebc98a0f61d2a5d95eecef3bd73db09468b43f281432335a45bc`  
		Last Modified: Wed, 26 Oct 2022 12:17:52 GMT  
		Size: 66.8 MB (66838109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf5689446f91a32b38aa40537221bd9f755abdd14ef57c1c9e10c6bc960ae113`  
		Last Modified: Wed, 26 Oct 2022 12:18:23 GMT  
		Size: 115.0 MB (115009090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18db3f2cd0257c72fed0154c965efda4550f0ee8fedbbd5b1d706d2928f3a319`  
		Last Modified: Wed, 26 Oct 2022 12:17:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:bullseye` - linux; ppc64le

```console
$ docker pull golang@sha256:209381adae6e1c8755a24926f0300f49c03f3527c4324405d90dba7303130b63
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.8 MB (330780532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86f700c521d30d5eccbcc8a49553afb1225938d7fc2d7427640ef399f932db7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:13:28 GMT
ADD file:c01a6cc4222fbeeda5c2d679c5b355539880a02c792c64861eb17b81a3678f45 in / 
# Tue, 25 Oct 2022 03:13:31 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:13:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:14:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 06:14:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 18:01:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 18:02:01 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Oct 2022 18:02:01 GMT
ENV GOLANG_VERSION=1.19.2
# Tue, 25 Oct 2022 18:02:25 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.19.2.linux-amd64.tar.gz'; 			sha256='5e8c5a74fe6470dd7e055a461acda8bb4050ead8c2df70f227e3ff7d8eb7eeb6'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.19.2.linux-armv6l.tar.gz'; 			sha256='f3ccec7816ecd704ebafd130b08b8ad97c55402a8193a107b63e9de12ab90118'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.19.2.linux-arm64.tar.gz'; 			sha256='b62a8d9654436c67c14a0c91e931d50440541f09eb991a987536cb982903126d'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.19.2.linux-386.tar.gz'; 			sha256='ba8c97965e0856c69c9ca2c86f96bec5bb21de43e6533e25494bb211d85cda1b'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.19.2.linux-ppc64le.tar.gz'; 			sha256='37e1d4342f7103aeb9babeabe8c71ef3dba23db28db525071119e94b2aa21d7d'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.19.2.linux-s390x.tar.gz'; 			sha256='51b45dec41295215df17f78e67d1a373b9dda97a5e539bed440974da5ffc97de'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.2.src.tar.gz'; 		sha256='2ce930d70a931de660fdaf271d70192793b1b240272645bf0275779f6704df6b'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Tue, 25 Oct 2022 18:02:30 GMT
ENV GOPATH=/go
# Tue, 25 Oct 2022 18:02:30 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Oct 2022 18:02:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 25 Oct 2022 18:02:32 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ee5a342763ed1d31bef8cebe9f4cc5dd6d427f630da679a87da0427be7b22e3d`  
		Last Modified: Tue, 25 Oct 2022 03:18:52 GMT  
		Size: 58.9 MB (58916374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a4727f39cbcb19b39abdbd847eeceed842ef65f8514372024c48b913bc951a`  
		Last Modified: Tue, 25 Oct 2022 06:49:00 GMT  
		Size: 5.4 MB (5414507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe601e6c8a1ec9c69c49c65a53339202a65cea9d4f01d161fb34905c06a4a99`  
		Last Modified: Tue, 25 Oct 2022 06:49:01 GMT  
		Size: 11.6 MB (11630153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5055e27b58426c2b637b1c8c179e6abe306e3dfb55a9c170c73fb0d581c6cf3e`  
		Last Modified: Tue, 25 Oct 2022 06:49:31 GMT  
		Size: 58.9 MB (58867355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf936729b2411f0eda4222e8d64bfbdb2bbab95aa679a5b404a8def8f316c53`  
		Last Modified: Tue, 25 Oct 2022 18:05:05 GMT  
		Size: 80.4 MB (80419664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eaa61f2b44db50532e706d455bbffda46470b28a5f2fee8339c5c54e03ca3a1`  
		Last Modified: Tue, 25 Oct 2022 18:05:10 GMT  
		Size: 115.5 MB (115532322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4723f0c3c4c63acf99b42245812411972386fcea9ae8ebb3df91e2ec220675f6`  
		Last Modified: Tue, 25 Oct 2022 18:04:43 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:bullseye` - linux; s390x

```console
$ docker pull golang@sha256:a3c44afdeca83482474b3ff6806c42d6efaabb3336c42abe5860dc63e3c363ae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.9 MB (307948691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9452e731aebabd734df603c357237f889f343d1c55d74ee86a9cf23a1fdc8743`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:14:24 GMT
ADD file:06f15d8a3c04752d271a052e820fb13fcdb76f0d18f6c9afb6e70391d10348ec in / 
# Tue, 25 Oct 2022 01:14:27 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:31:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 02:31:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 02:31:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 13:32:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 13:32:50 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Oct 2022 13:32:50 GMT
ENV GOLANG_VERSION=1.19.2
# Tue, 25 Oct 2022 13:33:03 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.19.2.linux-amd64.tar.gz'; 			sha256='5e8c5a74fe6470dd7e055a461acda8bb4050ead8c2df70f227e3ff7d8eb7eeb6'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.19.2.linux-armv6l.tar.gz'; 			sha256='f3ccec7816ecd704ebafd130b08b8ad97c55402a8193a107b63e9de12ab90118'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.19.2.linux-arm64.tar.gz'; 			sha256='b62a8d9654436c67c14a0c91e931d50440541f09eb991a987536cb982903126d'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.19.2.linux-386.tar.gz'; 			sha256='ba8c97965e0856c69c9ca2c86f96bec5bb21de43e6533e25494bb211d85cda1b'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.19.2.linux-ppc64le.tar.gz'; 			sha256='37e1d4342f7103aeb9babeabe8c71ef3dba23db28db525071119e94b2aa21d7d'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.19.2.linux-s390x.tar.gz'; 			sha256='51b45dec41295215df17f78e67d1a373b9dda97a5e539bed440974da5ffc97de'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.2.src.tar.gz'; 		sha256='2ce930d70a931de660fdaf271d70192793b1b240272645bf0275779f6704df6b'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Tue, 25 Oct 2022 13:33:08 GMT
ENV GOPATH=/go
# Tue, 25 Oct 2022 13:33:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Oct 2022 13:33:09 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 25 Oct 2022 13:33:09 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a556186e8bea4ba9925d0c17bea2c12bfbb931653cfab1b980036800482cf0ad`  
		Last Modified: Tue, 25 Oct 2022 01:18:39 GMT  
		Size: 53.3 MB (53279106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1e8478a953d3a464d73e36e4032c979725bc79ce0eeb83aca30212de549b90`  
		Last Modified: Tue, 25 Oct 2022 02:49:32 GMT  
		Size: 5.1 MB (5148477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cdbee45ed722bfaf7e9ba90503afa7a0cf17b87fc1bfa1e87cbf49ca6bd7d9`  
		Last Modified: Tue, 25 Oct 2022 02:49:33 GMT  
		Size: 10.8 MB (10766704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76aacd12f54fec6c8f627f09641ea144eb6fefeebc8f9fc35de80c3e3ab11af7`  
		Last Modified: Tue, 25 Oct 2022 02:49:48 GMT  
		Size: 54.1 MB (54055853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68c70a67df68f7eae963aff382c1a55a1a2aad6ef574ed61c74ee941dcacf29`  
		Last Modified: Tue, 25 Oct 2022 13:35:18 GMT  
		Size: 65.7 MB (65667297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dce66592be46807d0aa4cb2e80933b7432b9c2ae3031ba62a5ef62265044517`  
		Last Modified: Tue, 25 Oct 2022 13:35:24 GMT  
		Size: 119.0 MB (119031099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c951817387866d3e7676b35dd901ff1df4f0cb7e347be4020046dd80559fc7`  
		Last Modified: Tue, 25 Oct 2022 13:35:10 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
