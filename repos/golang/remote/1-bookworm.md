## `golang:1-bookworm`

```console
$ docker pull golang@sha256:df6e0575fa85112451fdc208d372fc724294b093c7a5395000eca92e68b52c46
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

### `golang:1-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:0dff643e5bf836005eea93ad89e084a17681173e54dbaa9ec307fd776acab36e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.0 MB (296956359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ca605b665e9e777d46d3de2a8c4efd1a2da5128a63bde24943b13b1ef0b999`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 00:20:39 GMT
ADD file:8415eb847ca46ed1aa1695965af86f1a0f09e8859a7b3c07b2f719404b665102 in / 
# Thu, 07 Sep 2023 00:20:39 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 02:56:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 02:56:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 20:09:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 20:09:40 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 20:09:40 GMT
ENV GOLANG_VERSION=1.21.1
# Thu, 07 Sep 2023 20:09:48 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.1.linux-amd64.tar.gz'; 			sha256='b3075ae1ce5dab85f89bc7905d1632de23ca196bd8336afd93fa97434cfa55ae'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.1.linux-armv6l.tar.gz'; 			sha256='f3716a43f59ae69999841d6007b42c9e286e8d8ce470656fb3e70d7be2d7ca85'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.1.linux-arm64.tar.gz'; 			sha256='7da1a3936a928fd0b2602ed4f3ef535b8cd1990f1503b8d3e1acc0fa0759c967'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.1.linux-386.tar.gz'; 			sha256='b93850666cdadbd696a986cf7b03111fe99db8c34a9aaa113d7c96d0081e1901'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.1.linux-mips64le.tar.gz'; 			sha256='3aa007a41f533b50eae2491bbd29926ada09357367a8aa05e7e50ec50c78acf9'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.1.linux-ppc64le.tar.gz'; 			sha256='eddf018206f8a5589bda75252b72716d26611efebabdca5d0083ec15e9e41ab7'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.1.linux-riscv64.tar.gz'; 			sha256='fac64ed26e003f49f1d77f6d2c4cf951422aecbce12232d9ec1bf4585fc44ee1'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.1.linux-s390x.tar.gz'; 			sha256='a83b3e8eb4dbf76294e773055eb51397510ff4d612a247bad9903560267bba6d'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.1.src.tar.gz'; 		sha256='bfa36bf75e9a1e9cbbdb9abcf9d1707e479bd3a07880a8ae3564caee5711cb99'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Thu, 07 Sep 2023 20:09:49 GMT
ENV GOPATH=/go
# Thu, 07 Sep 2023 20:09:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 20:09:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Thu, 07 Sep 2023 20:09:50 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:012c0b3e998c1a0c0bedcf712eaaafb188580529dd026a04aa1ce13fdb39e42b`  
		Last Modified: Thu, 07 Sep 2023 00:24:59 GMT  
		Size: 49.6 MB (49557216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00046d1e755ea94fa55a700ca9a10597e4fac7c47be19d970a359b0267a51fbf`  
		Last Modified: Thu, 07 Sep 2023 03:04:41 GMT  
		Size: 24.0 MB (24030451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f13f5a53d118643c1f1ff294867c09f224d00edca21f56caa71c2321f8ca004`  
		Last Modified: Thu, 07 Sep 2023 03:05:02 GMT  
		Size: 64.1 MB (64112250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:190fa1651026077cee00b53a754acbe0dc734b99255c6b274e798f6cd877ae18`  
		Last Modified: Thu, 07 Sep 2023 20:11:36 GMT  
		Size: 92.3 MB (92267037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23daf7e716100b927e5375d374665c503315a4afe969079e57c141003a30c9d4`  
		Last Modified: Thu, 07 Sep 2023 20:11:34 GMT  
		Size: 67.0 MB (66989250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94830e2a7523c5b5c0fa14d9fa623aa1cf851333c6d979164f74d8a35366ea2f`  
		Last Modified: Thu, 07 Sep 2023 20:11:22 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; arm variant v5

```console
$ docker pull golang@sha256:29ba3db9db57216d02d893f4349e9a033ed0a040c2672fa41df49807c84305f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.2 MB (271228743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee7ef2e7e2b7a5f20ccaf965222fadf880eca22f1d3cd667045343fe7024843`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 00:48:22 GMT
ADD file:a521640a9f8215118db986479d0ac7e8fae5d186fe5d1c069c166217e63c45a0 in / 
# Thu, 07 Sep 2023 00:48:23 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 06:15:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 06:15:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 15:27:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 15:27:58 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 15:27:58 GMT
ENV GOLANG_VERSION=1.21.1
# Thu, 07 Sep 2023 15:30:27 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.1.linux-amd64.tar.gz'; 			sha256='b3075ae1ce5dab85f89bc7905d1632de23ca196bd8336afd93fa97434cfa55ae'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.1.linux-armv6l.tar.gz'; 			sha256='f3716a43f59ae69999841d6007b42c9e286e8d8ce470656fb3e70d7be2d7ca85'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.1.linux-arm64.tar.gz'; 			sha256='7da1a3936a928fd0b2602ed4f3ef535b8cd1990f1503b8d3e1acc0fa0759c967'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.1.linux-386.tar.gz'; 			sha256='b93850666cdadbd696a986cf7b03111fe99db8c34a9aaa113d7c96d0081e1901'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.1.linux-mips64le.tar.gz'; 			sha256='3aa007a41f533b50eae2491bbd29926ada09357367a8aa05e7e50ec50c78acf9'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.1.linux-ppc64le.tar.gz'; 			sha256='eddf018206f8a5589bda75252b72716d26611efebabdca5d0083ec15e9e41ab7'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.1.linux-riscv64.tar.gz'; 			sha256='fac64ed26e003f49f1d77f6d2c4cf951422aecbce12232d9ec1bf4585fc44ee1'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.1.linux-s390x.tar.gz'; 			sha256='a83b3e8eb4dbf76294e773055eb51397510ff4d612a247bad9903560267bba6d'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.1.src.tar.gz'; 		sha256='bfa36bf75e9a1e9cbbdb9abcf9d1707e479bd3a07880a8ae3564caee5711cb99'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Thu, 07 Sep 2023 15:30:30 GMT
ENV GOPATH=/go
# Thu, 07 Sep 2023 15:30:30 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 15:30:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Thu, 07 Sep 2023 15:30:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:665aaf2dc96ac62bc1e5597eccfa5152d16607f9b620eb4b87b2bb76f0c58104`  
		Last Modified: Thu, 07 Sep 2023 00:51:04 GMT  
		Size: 47.4 MB (47414921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0abb06146a2816f483c23584b16206d93e3536ec201cf895f04965d36df091d`  
		Last Modified: Thu, 07 Sep 2023 06:24:46 GMT  
		Size: 22.7 MB (22709691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f40fe741e3fe03814b1e440e0b95b2df1442530abd3ab735841089bf8d575ea`  
		Last Modified: Thu, 07 Sep 2023 06:25:07 GMT  
		Size: 61.6 MB (61554132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7e726d1eaa2f0dfac3cf65b71d3a5726641358859b348d93514ae91d60c095`  
		Last Modified: Thu, 07 Sep 2023 15:38:55 GMT  
		Size: 71.3 MB (71279570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f1e8e23b9f1743f5d2de0bfdae8f9f3dcb921fbbcc9dcbb108df3e83518d27`  
		Last Modified: Thu, 07 Sep 2023 15:38:57 GMT  
		Size: 68.3 MB (68270273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20a25db135be99871d59d2893ecc4f2af67f67a542d6dc9ed3531789567c9c0`  
		Last Modified: Thu, 07 Sep 2023 15:38:42 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:9bf3c05b0197c8695c9ba12d3d8fed0c8ad4e71c91ef7cdd0fe804eb67434748
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.3 MB (258300322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d8faf032875569a3b7e9cf697122fff054610e9da372dee662db9b4220465a5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 00:57:31 GMT
ADD file:33a39c01d7e209fab46b54083ee271e3bdd3d4dccc3a6e8635cbe0989c92c53e in / 
# Thu, 07 Sep 2023 00:57:33 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 01:33:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 01:33:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 19:28:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 19:28:34 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 19:28:34 GMT
ENV GOLANG_VERSION=1.21.1
# Thu, 07 Sep 2023 19:28:48 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.1.linux-amd64.tar.gz'; 			sha256='b3075ae1ce5dab85f89bc7905d1632de23ca196bd8336afd93fa97434cfa55ae'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.1.linux-armv6l.tar.gz'; 			sha256='f3716a43f59ae69999841d6007b42c9e286e8d8ce470656fb3e70d7be2d7ca85'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.1.linux-arm64.tar.gz'; 			sha256='7da1a3936a928fd0b2602ed4f3ef535b8cd1990f1503b8d3e1acc0fa0759c967'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.1.linux-386.tar.gz'; 			sha256='b93850666cdadbd696a986cf7b03111fe99db8c34a9aaa113d7c96d0081e1901'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.1.linux-mips64le.tar.gz'; 			sha256='3aa007a41f533b50eae2491bbd29926ada09357367a8aa05e7e50ec50c78acf9'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.1.linux-ppc64le.tar.gz'; 			sha256='eddf018206f8a5589bda75252b72716d26611efebabdca5d0083ec15e9e41ab7'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.1.linux-riscv64.tar.gz'; 			sha256='fac64ed26e003f49f1d77f6d2c4cf951422aecbce12232d9ec1bf4585fc44ee1'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.1.linux-s390x.tar.gz'; 			sha256='a83b3e8eb4dbf76294e773055eb51397510ff4d612a247bad9903560267bba6d'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.1.src.tar.gz'; 		sha256='bfa36bf75e9a1e9cbbdb9abcf9d1707e479bd3a07880a8ae3564caee5711cb99'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Thu, 07 Sep 2023 19:28:49 GMT
ENV GOPATH=/go
# Thu, 07 Sep 2023 19:28:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 19:28:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Thu, 07 Sep 2023 19:28:50 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4e1ef44b7a1dc38ec98ec01f961a48844fdf07e1ff182d55daae1c01406302a9`  
		Last Modified: Thu, 07 Sep 2023 01:02:04 GMT  
		Size: 45.2 MB (45233200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c71aa39a4f5a50ddeb9942b08a954d6892177b5409397b1e948e88ac7f6575a`  
		Last Modified: Thu, 07 Sep 2023 01:44:56 GMT  
		Size: 21.9 MB (21936900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783a38d6b0b707ea959723e364564dbc0237dc7dade3fca851cb6cac5ca4557d`  
		Last Modified: Thu, 07 Sep 2023 01:45:20 GMT  
		Size: 59.3 MB (59262020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790e69e65b5407ef01693274d13b3845966b5df22618899c6f640b51c4408815`  
		Last Modified: Thu, 07 Sep 2023 19:30:52 GMT  
		Size: 66.1 MB (66119416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765309475ebd8e2da23246bea716078e4aab9f71be957ce50981ec089d332e7e`  
		Last Modified: Thu, 07 Sep 2023 19:30:56 GMT  
		Size: 65.7 MB (65748631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3ffc48108b1161ec67d183f3efe126f46869d2df077f27f2b1c449e849c999`  
		Last Modified: Thu, 07 Sep 2023 19:30:43 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:d6df8b2e22c9c87fde828b18e0d0d5707bfe03034a49c0bde72ff5a1f5ebb5fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287534354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edf959ea934af5037dacb80612e27e6019a78f944c5ff33fc3bb2bc967c619b5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:31 GMT
ADD file:f9dd2b1cc0ba261acd8a3e500c54f6b6e0a46131a32988bfd71cf3c6fc5a7d13 in / 
# Thu, 07 Sep 2023 00:39:32 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 06:51:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 06:51:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 11:03:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 11:03:05 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 11:03:05 GMT
ENV GOLANG_VERSION=1.21.1
# Thu, 07 Sep 2023 11:03:13 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.1.linux-amd64.tar.gz'; 			sha256='b3075ae1ce5dab85f89bc7905d1632de23ca196bd8336afd93fa97434cfa55ae'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.1.linux-armv6l.tar.gz'; 			sha256='f3716a43f59ae69999841d6007b42c9e286e8d8ce470656fb3e70d7be2d7ca85'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.1.linux-arm64.tar.gz'; 			sha256='7da1a3936a928fd0b2602ed4f3ef535b8cd1990f1503b8d3e1acc0fa0759c967'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.1.linux-386.tar.gz'; 			sha256='b93850666cdadbd696a986cf7b03111fe99db8c34a9aaa113d7c96d0081e1901'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.1.linux-mips64le.tar.gz'; 			sha256='3aa007a41f533b50eae2491bbd29926ada09357367a8aa05e7e50ec50c78acf9'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.1.linux-ppc64le.tar.gz'; 			sha256='eddf018206f8a5589bda75252b72716d26611efebabdca5d0083ec15e9e41ab7'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.1.linux-riscv64.tar.gz'; 			sha256='fac64ed26e003f49f1d77f6d2c4cf951422aecbce12232d9ec1bf4585fc44ee1'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.1.linux-s390x.tar.gz'; 			sha256='a83b3e8eb4dbf76294e773055eb51397510ff4d612a247bad9903560267bba6d'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.1.src.tar.gz'; 		sha256='bfa36bf75e9a1e9cbbdb9abcf9d1707e479bd3a07880a8ae3564caee5711cb99'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Thu, 07 Sep 2023 11:03:14 GMT
ENV GOPATH=/go
# Thu, 07 Sep 2023 11:03:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 11:03:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Thu, 07 Sep 2023 11:03:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fa34261389f3dee2ecffe9bfe38ae7fd05a1908e98a7486354905aee0f648a6e`  
		Last Modified: Thu, 07 Sep 2023 00:42:39 GMT  
		Size: 49.6 MB (49590783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993525952a483617183655b735562fd3eee4b3a85a472e3dc3c79a258adca100`  
		Last Modified: Thu, 07 Sep 2023 06:59:20 GMT  
		Size: 23.6 MB (23570086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12916f73f9de8e251c4eb4f2d079fa6cd63205b7ba8a7bd88e1f9446105e9ef1`  
		Last Modified: Thu, 07 Sep 2023 06:59:37 GMT  
		Size: 64.0 MB (63988504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b84cd7f173d9c2c1287768f308d87cd738f9b833164dafc86f19453b6204a6e`  
		Last Modified: Thu, 07 Sep 2023 11:04:51 GMT  
		Size: 86.3 MB (86295575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226e4d0fab627acc81adc6b5468f96f387f381e03333444857ee2733cf99d057`  
		Last Modified: Thu, 07 Sep 2023 11:04:50 GMT  
		Size: 64.1 MB (64089250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b35d9d4068c4149e858f1ee9adf96a4cfb31a78087bb6a8828522fb15b6b3`  
		Last Modified: Thu, 07 Sep 2023 11:04:42 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; 386

```console
$ docker pull golang@sha256:44671959ce53714e81dd3a1ff1d66bf1bd5b3daea3f794f628ff18f377ca0b29
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.5 MB (296525276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73f913af7853c8f1b87af241e96f37f6c345fc4b0593b0a766e038a29380c9cb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Aug 2023 23:38:49 GMT
ADD file:3f0a4d6b18b22088d0785bc2e351d829ad1ed6f154058017035842bdbe2a8d1e in / 
# Tue, 15 Aug 2023 23:38:51 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 00:25:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 00:26:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 20:34:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 20:34:45 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Sep 2023 18:30:51 GMT
ENV GOLANG_VERSION=1.21.1
# Wed, 06 Sep 2023 18:31:06 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.1.linux-amd64.tar.gz'; 			sha256='b3075ae1ce5dab85f89bc7905d1632de23ca196bd8336afd93fa97434cfa55ae'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.1.linux-armv6l.tar.gz'; 			sha256='f3716a43f59ae69999841d6007b42c9e286e8d8ce470656fb3e70d7be2d7ca85'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.1.linux-arm64.tar.gz'; 			sha256='7da1a3936a928fd0b2602ed4f3ef535b8cd1990f1503b8d3e1acc0fa0759c967'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.1.linux-386.tar.gz'; 			sha256='b93850666cdadbd696a986cf7b03111fe99db8c34a9aaa113d7c96d0081e1901'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.1.linux-mips64le.tar.gz'; 			sha256='3aa007a41f533b50eae2491bbd29926ada09357367a8aa05e7e50ec50c78acf9'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.1.linux-ppc64le.tar.gz'; 			sha256='eddf018206f8a5589bda75252b72716d26611efebabdca5d0083ec15e9e41ab7'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.1.linux-riscv64.tar.gz'; 			sha256='fac64ed26e003f49f1d77f6d2c4cf951422aecbce12232d9ec1bf4585fc44ee1'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.1.linux-s390x.tar.gz'; 			sha256='a83b3e8eb4dbf76294e773055eb51397510ff4d612a247bad9903560267bba6d'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.1.src.tar.gz'; 		sha256='bfa36bf75e9a1e9cbbdb9abcf9d1707e479bd3a07880a8ae3564caee5711cb99'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Wed, 06 Sep 2023 18:31:08 GMT
ENV GOPATH=/go
# Wed, 06 Sep 2023 18:31:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Sep 2023 18:31:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Wed, 06 Sep 2023 18:31:08 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1dc6cc826af02d533745c4612f635e028f3471e46f50422fd20a6dc913b60574`  
		Last Modified: Tue, 15 Aug 2023 23:43:02 GMT  
		Size: 50.6 MB (50568054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ca8436c5a9dc8b9ea408612ff7210bcceebd896671ed3e31c61f398f9a00f25`  
		Last Modified: Wed, 16 Aug 2023 00:34:36 GMT  
		Size: 24.9 MB (24869754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4ec215b1e0b3f7f5034048ddb02b52122b17ef3885d242da7fca37250884e3`  
		Last Modified: Wed, 16 Aug 2023 00:35:00 GMT  
		Size: 66.0 MB (65972400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3534d5cc9b58d68e1ac673d9b3a51a0e865066cefa3841839d934b5576f2f3cc`  
		Last Modified: Wed, 16 Aug 2023 20:37:11 GMT  
		Size: 89.7 MB (89672339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3278f4b6f74678fec69c4c5909e4b4a31e3c90f958b1b4501fdea320a1c4fe0`  
		Last Modified: Wed, 06 Sep 2023 18:40:04 GMT  
		Size: 65.4 MB (65442574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ec3f495da1b8f643ff7fac3f3e7de10381087e64e1afa5bc52552d72ab4781`  
		Last Modified: Wed, 06 Sep 2023 18:39:47 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:76f70b630b28784483eee85e251da120be19b6ab8510a764bb3a5679d6dd80f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.9 MB (267858948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53c5127902025a3c2f6e004fa273d3bdd6caf84ba2adab48a69ce51663444e5e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 00:08:02 GMT
ADD file:359d49b8d6eb4185590cb5da2825a99e2b2d4b4d81519b9283794e64261eec2c in / 
# Wed, 16 Aug 2023 00:08:08 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 14:33:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 14:35:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 16:15:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 16:15:36 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Sep 2023 18:31:14 GMT
ENV GOLANG_VERSION=1.21.1
# Wed, 06 Sep 2023 18:32:05 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.1.linux-amd64.tar.gz'; 			sha256='b3075ae1ce5dab85f89bc7905d1632de23ca196bd8336afd93fa97434cfa55ae'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.1.linux-armv6l.tar.gz'; 			sha256='f3716a43f59ae69999841d6007b42c9e286e8d8ce470656fb3e70d7be2d7ca85'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.1.linux-arm64.tar.gz'; 			sha256='7da1a3936a928fd0b2602ed4f3ef535b8cd1990f1503b8d3e1acc0fa0759c967'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.1.linux-386.tar.gz'; 			sha256='b93850666cdadbd696a986cf7b03111fe99db8c34a9aaa113d7c96d0081e1901'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.1.linux-mips64le.tar.gz'; 			sha256='3aa007a41f533b50eae2491bbd29926ada09357367a8aa05e7e50ec50c78acf9'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.1.linux-ppc64le.tar.gz'; 			sha256='eddf018206f8a5589bda75252b72716d26611efebabdca5d0083ec15e9e41ab7'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.1.linux-riscv64.tar.gz'; 			sha256='fac64ed26e003f49f1d77f6d2c4cf951422aecbce12232d9ec1bf4585fc44ee1'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.1.linux-s390x.tar.gz'; 			sha256='a83b3e8eb4dbf76294e773055eb51397510ff4d612a247bad9903560267bba6d'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.1.src.tar.gz'; 		sha256='bfa36bf75e9a1e9cbbdb9abcf9d1707e479bd3a07880a8ae3564caee5711cb99'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Wed, 06 Sep 2023 18:32:13 GMT
ENV GOPATH=/go
# Wed, 06 Sep 2023 18:32:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Sep 2023 18:32:29 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Wed, 06 Sep 2023 18:32:36 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:96b8a462ea6d525b430e77289e7ae92006277c062da33a8446fd1e664d41600b`  
		Last Modified: Wed, 16 Aug 2023 00:18:49 GMT  
		Size: 49.5 MB (49542000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8a8c9ea13a792b89577cb50edc4ddd2f4e3530348051c8c3a6d83065301bca`  
		Last Modified: Wed, 16 Aug 2023 15:00:21 GMT  
		Size: 23.6 MB (23612660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85b30253a84fcbbec4217a75f594587c3eda3f23774859a9d945f37da28e1dad`  
		Last Modified: Wed, 16 Aug 2023 15:01:15 GMT  
		Size: 63.0 MB (62950874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613fc4a15979681f5cc1c82a9dca28e9cf59ef5f7939591ced99533f2f94f85f`  
		Last Modified: Wed, 16 Aug 2023 16:46:40 GMT  
		Size: 69.6 MB (69624276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aadde54c7c6a7d5e779475b5e7ed42805e4b9820015c85366be2cb5c0ecc45f`  
		Last Modified: Wed, 06 Sep 2023 19:01:26 GMT  
		Size: 62.1 MB (62129013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd4409270dde1ceed2ff089405b35b5c58c7394166f26688fe2c1dc69bbd55f`  
		Last Modified: Wed, 06 Sep 2023 19:00:35 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:8c51bdc2812b00f61772e7e56a0d24957f6bc11d3c6bf745c3ef45e4dfde2f1f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.2 MB (303158178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2503019ab3055afda7465c90b105800433f4fc0813c0a275d6d97e81b5a64623`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Aug 2023 01:09:14 GMT
ADD file:8397677919f9bbf5273ddf61e008bcaace9195b46bcb2c31aff4f0a88617f12e in / 
# Wed, 16 Aug 2023 01:09:17 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:38:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 01:39:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:05:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:05:27 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Sep 2023 18:31:04 GMT
ENV GOLANG_VERSION=1.21.1
# Wed, 06 Sep 2023 18:31:26 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.1.linux-amd64.tar.gz'; 			sha256='b3075ae1ce5dab85f89bc7905d1632de23ca196bd8336afd93fa97434cfa55ae'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.1.linux-armv6l.tar.gz'; 			sha256='f3716a43f59ae69999841d6007b42c9e286e8d8ce470656fb3e70d7be2d7ca85'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.1.linux-arm64.tar.gz'; 			sha256='7da1a3936a928fd0b2602ed4f3ef535b8cd1990f1503b8d3e1acc0fa0759c967'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.1.linux-386.tar.gz'; 			sha256='b93850666cdadbd696a986cf7b03111fe99db8c34a9aaa113d7c96d0081e1901'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.1.linux-mips64le.tar.gz'; 			sha256='3aa007a41f533b50eae2491bbd29926ada09357367a8aa05e7e50ec50c78acf9'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.1.linux-ppc64le.tar.gz'; 			sha256='eddf018206f8a5589bda75252b72716d26611efebabdca5d0083ec15e9e41ab7'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.1.linux-riscv64.tar.gz'; 			sha256='fac64ed26e003f49f1d77f6d2c4cf951422aecbce12232d9ec1bf4585fc44ee1'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.1.linux-s390x.tar.gz'; 			sha256='a83b3e8eb4dbf76294e773055eb51397510ff4d612a247bad9903560267bba6d'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.1.src.tar.gz'; 		sha256='bfa36bf75e9a1e9cbbdb9abcf9d1707e479bd3a07880a8ae3564caee5711cb99'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Wed, 06 Sep 2023 18:31:30 GMT
ENV GOPATH=/go
# Wed, 06 Sep 2023 18:31:30 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Sep 2023 18:31:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Wed, 06 Sep 2023 18:31:33 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c59f7b2759f74830e13fa72caeaf898f560f72787aa9d5aec28bcf8585f2f066`  
		Last Modified: Wed, 16 Aug 2023 01:15:22 GMT  
		Size: 53.5 MB (53543761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cce374dd487e4d067dd2727a6401d31bd379da6e10a83e5a902a80be18aabaf`  
		Last Modified: Wed, 16 Aug 2023 02:09:27 GMT  
		Size: 25.7 MB (25681124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acab4f12553730c8f77e5e6b7ef103cdaf3f7db095c145c4b58ec1da135086b1`  
		Last Modified: Wed, 16 Aug 2023 02:09:59 GMT  
		Size: 69.6 MB (69570024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4dd17847b9fbcafa06a2a520f1b6b4bac508660bb01ca6cb921fe0914fa12d`  
		Last Modified: Thu, 17 Aug 2023 07:10:34 GMT  
		Size: 90.3 MB (90251857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f5368e5b50042c5a1767306407e3adb6515c056e310f2a233af00c0c91100b0`  
		Last Modified: Wed, 06 Sep 2023 18:42:44 GMT  
		Size: 64.1 MB (64111257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f91d5619779915694cb651caed6f42b07706b510baa6a53c2a6b38b8b326d9`  
		Last Modified: Wed, 06 Sep 2023 18:42:26 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:91746f544a025112fd767f187552db4ba2ff20f0db731e1cfeb4ddf2a2aa15d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.1 MB (270093860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a7534763eee7a7d9d83c64231ce38034905635163d6fc5608bfec373d1028e4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 07 Sep 2023 00:43:05 GMT
ADD file:b24f18eeabdca57806be7cfa8dd6a173a7448efe4c914018c8f2b2f11f973a75 in / 
# Thu, 07 Sep 2023 00:43:16 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 01:10:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 01:10:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 16:55:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 16:55:36 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 16:55:36 GMT
ENV GOLANG_VERSION=1.21.1
# Thu, 07 Sep 2023 16:55:46 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.21.1.linux-amd64.tar.gz'; 			sha256='b3075ae1ce5dab85f89bc7905d1632de23ca196bd8336afd93fa97434cfa55ae'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.21.1.linux-armv6l.tar.gz'; 			sha256='f3716a43f59ae69999841d6007b42c9e286e8d8ce470656fb3e70d7be2d7ca85'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.21.1.linux-arm64.tar.gz'; 			sha256='7da1a3936a928fd0b2602ed4f3ef535b8cd1990f1503b8d3e1acc0fa0759c967'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.21.1.linux-386.tar.gz'; 			sha256='b93850666cdadbd696a986cf7b03111fe99db8c34a9aaa113d7c96d0081e1901'; 			;; 		'mips64el') 			url='https://dl.google.com/go/go1.21.1.linux-mips64le.tar.gz'; 			sha256='3aa007a41f533b50eae2491bbd29926ada09357367a8aa05e7e50ec50c78acf9'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.21.1.linux-ppc64le.tar.gz'; 			sha256='eddf018206f8a5589bda75252b72716d26611efebabdca5d0083ec15e9e41ab7'; 			;; 		'riscv64') 			url='https://dl.google.com/go/go1.21.1.linux-riscv64.tar.gz'; 			sha256='fac64ed26e003f49f1d77f6d2c4cf951422aecbce12232d9ec1bf4585fc44ee1'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.21.1.linux-s390x.tar.gz'; 			sha256='a83b3e8eb4dbf76294e773055eb51397510ff4d612a247bad9903560267bba6d'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.21.1.src.tar.gz'; 		sha256='bfa36bf75e9a1e9cbbdb9abcf9d1707e479bd3a07880a8ae3564caee5711cb99'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Thu, 07 Sep 2023 16:55:51 GMT
ENV GOPATH=/go
# Thu, 07 Sep 2023 16:55:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 16:55:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Thu, 07 Sep 2023 16:55:52 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:057281f9e836e5a46ec8be5758de3606940b3a68408826bb8ce7a512f3cb0e70`  
		Last Modified: Thu, 07 Sep 2023 00:49:22 GMT  
		Size: 47.9 MB (47921986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fae8fcf22d3d3b48cf6401a63ae5533b13aa37cc17f3d8b25b809b05961b5e6`  
		Last Modified: Thu, 07 Sep 2023 01:22:09 GMT  
		Size: 24.0 MB (24028757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c49a6ed043db6d0813d84662b4c92ab40cb9dba09cd69b24463600608b8e8e53`  
		Last Modified: Thu, 07 Sep 2023 01:22:26 GMT  
		Size: 63.1 MB (63113093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c994597052291c7040941e454aefd572f2ff60dd9b6f68d6d8e02942511941`  
		Last Modified: Thu, 07 Sep 2023 16:58:47 GMT  
		Size: 68.8 MB (68826484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9258f0f8ed416804709914e91aee39691e4d65c03bf028d62662eaae64bcda39`  
		Last Modified: Thu, 07 Sep 2023 16:58:49 GMT  
		Size: 66.2 MB (66203383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5254552de5705391253be15e6ce51ab4ab71bfdca59b6cefcfe21eafec55241b`  
		Last Modified: Thu, 07 Sep 2023 16:58:38 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
