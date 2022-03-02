## `golang:rc-bullseye`

```console
$ docker pull golang@sha256:30e402fdccce403eeebed4f406b4d60fdcd187ed085b56919edf6215c309de93
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

### `golang:rc-bullseye` - linux; amd64

```console
$ docker pull golang@sha256:cb3797dbc21abc9647aa23cdb36e3817e056f0703230bf6a4f3b53795fe51882
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.0 MB (352965864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76b61db4adeaf84a7016e12cecb0bf6fef7996eb150356d23932ce1677239c41`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:15 GMT
ADD file:9c4db2a9644ee3029a8e9cca58350efef660c3167e59b91f2bee9c303e592664 in / 
# Tue, 01 Mar 2022 02:13:15 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 06:25:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 06:26:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 06:26:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 17:51:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 17:51:28 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Mar 2022 17:51:28 GMT
ENV GOLANG_VERSION=1.18rc1
# Wed, 02 Mar 2022 17:52:54 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18rc1.linux-amd64.tar.gz'; 			sha256='9ea4e6adee711e06fa95546e1a9629b63de3aaae85fac9dc752fb533f3e5be23'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18rc1.linux-armv6l.tar.gz'; 			sha256='d7a3f97b23b1e1f2e1a3596ff011e78f93aa8bbd991e2065ac34c18993884ea1'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18rc1.linux-arm64.tar.gz'; 			sha256='e4528a113016872a3715cec37a6c6dad36d76d51a50fa19b33b7673e47e6df44'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18rc1.linux-386.tar.gz'; 			sha256='a4bb0097276fa3523f1ce84dc4ee50fab0b3b0f7fbe72833710434889516c51e'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18rc1.linux-ppc64le.tar.gz'; 			sha256='a2944dfc3ee22efe1b940f122ee36cb4bb446e209116e5e8f244e78682ece981'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18rc1.linux-s390x.tar.gz'; 			sha256='e5578b8cbcc90659496f3930c61c6974c039d32d0573a6726c5d8e62f7e42d68'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18rc1.src.tar.gz'; 		sha256='5cec7a6653008fa85f8821b33665de37be289b7a02f17f36f705a88c43980bb8'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 02 Mar 2022 17:52:57 GMT
ENV GOPATH=/go
# Wed, 02 Mar 2022 17:52:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Mar 2022 17:52:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 02 Mar 2022 17:52:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e4d61adff2077d048c6372d73c41b0bd68f525ad41f5530af05098a876683055`  
		Last Modified: Tue, 01 Mar 2022 02:18:55 GMT  
		Size: 54.9 MB (54917063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff1945c672b08a1791df62afaaf8aff14d3047155365f9c3646902937f7ffe6`  
		Last Modified: Tue, 01 Mar 2022 06:36:13 GMT  
		Size: 5.2 MB (5153034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5b10aec998344606441aec43a335ab6326f32aae331aab27da16a6bb4ec2be`  
		Last Modified: Tue, 01 Mar 2022 06:36:14 GMT  
		Size: 10.9 MB (10871885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12de8c754e45686ace9e25d11bee372b070eed5b5ab20aa3b4fab8c936496d02`  
		Last Modified: Tue, 01 Mar 2022 06:36:38 GMT  
		Size: 54.6 MB (54575903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c86ff77a3175ed4d7958578d141a96b5da005855d60ea24067de33cd62e4c36`  
		Last Modified: Wed, 02 Mar 2022 18:06:15 GMT  
		Size: 85.8 MB (85811039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f641a927c5adc9f33d47352a15b16b60b55df79029ecf387dd8f849e6141f2c0`  
		Last Modified: Wed, 02 Mar 2022 18:06:24 GMT  
		Size: 141.6 MB (141636784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8599739dfb59c87b87993a21281dc9b49eda132205e6525673130d36574b6b`  
		Last Modified: Wed, 02 Mar 2022 18:06:00 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-bullseye` - linux; arm variant v5

```console
$ docker pull golang@sha256:e86e1ffa5dae8a5444cf4d4f861ebcc210e8192a00b8aca8e7e721c70b533007
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.6 MB (301569222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2a3ec95f8737861fa8d596297b93c47bd383b713a7cf80bc2178c78add8b7a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:02:16 GMT
ADD file:0c2b44806c285448ad64aefbcb64aed5f35092f4793649f111166170ebe1acd8 in / 
# Tue, 01 Mar 2022 02:02:17 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 03:01:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 03:01:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 03:02:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 07:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 07:40:16 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Mar 2022 07:40:17 GMT
ENV GOLANG_VERSION=1.18rc1
# Wed, 02 Mar 2022 07:44:51 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18rc1.linux-amd64.tar.gz'; 			sha256='9ea4e6adee711e06fa95546e1a9629b63de3aaae85fac9dc752fb533f3e5be23'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18rc1.linux-armv6l.tar.gz'; 			sha256='d7a3f97b23b1e1f2e1a3596ff011e78f93aa8bbd991e2065ac34c18993884ea1'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18rc1.linux-arm64.tar.gz'; 			sha256='e4528a113016872a3715cec37a6c6dad36d76d51a50fa19b33b7673e47e6df44'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18rc1.linux-386.tar.gz'; 			sha256='a4bb0097276fa3523f1ce84dc4ee50fab0b3b0f7fbe72833710434889516c51e'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18rc1.linux-ppc64le.tar.gz'; 			sha256='a2944dfc3ee22efe1b940f122ee36cb4bb446e209116e5e8f244e78682ece981'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18rc1.linux-s390x.tar.gz'; 			sha256='e5578b8cbcc90659496f3930c61c6974c039d32d0573a6726c5d8e62f7e42d68'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18rc1.src.tar.gz'; 		sha256='5cec7a6653008fa85f8821b33665de37be289b7a02f17f36f705a88c43980bb8'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 02 Mar 2022 07:44:53 GMT
ENV GOPATH=/go
# Wed, 02 Mar 2022 07:44:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Mar 2022 07:44:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 02 Mar 2022 07:44:55 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:27773abfb39f21d73b063cdbf05c7cb738d04f3443d6809d27fbfba465f7bb8f`  
		Last Modified: Tue, 01 Mar 2022 02:17:45 GMT  
		Size: 52.5 MB (52466222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61672d2178448aa6a4061114674fed9f190fbde42fc162b298c8a4a1224a95c8`  
		Last Modified: Tue, 01 Mar 2022 03:24:29 GMT  
		Size: 5.1 MB (5063741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6533a8a01b5bdac855422831efe7c334260d9865915e5ddaa9d7fc7019dd268`  
		Last Modified: Tue, 01 Mar 2022 03:24:31 GMT  
		Size: 10.6 MB (10570972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e3ce6e0b0fe54214cdb4a4ff48f54a0dcee2361b6c82f156b0e8597e9759ab`  
		Last Modified: Tue, 01 Mar 2022 03:25:24 GMT  
		Size: 52.3 MB (52319086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a09aa29756af4a48e989ad630f9d406c790d060dad8491fee9512e1dea9bdf`  
		Last Modified: Wed, 02 Mar 2022 08:08:43 GMT  
		Size: 68.7 MB (68739355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2429f3d06a3e8c936f4871cc943b967e17d3025cb4d18838271aa932d9d4c2e0`  
		Last Modified: Wed, 02 Mar 2022 08:09:14 GMT  
		Size: 112.4 MB (112409690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719c6b1d3a9509074f7ee619db00ab5da52951de5974a68dbfeeb59cb3c26d55`  
		Last Modified: Wed, 02 Mar 2022 08:08:01 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:1a5e8c0d7f3d8f4d0b081b66ac9fb1b4d98073632725c2124edb73e829f204be
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.3 MB (290322340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd66d94c48f161183cf8b43eb09898add5063dd94ca7b46561bf4b32dc3824a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:41:30 GMT
ADD file:19419917274a4a5aa3eceb0a6202f89e5b508368314f2bd0105897a847db4930 in / 
# Wed, 26 Jan 2022 01:41:31 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 16:37:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 16:38:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 16:38:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 20:30:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 20:30:07 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Feb 2022 04:20:36 GMT
ENV GOLANG_VERSION=1.18rc1
# Fri, 18 Feb 2022 04:21:29 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18rc1.linux-amd64.tar.gz'; 			sha256='9ea4e6adee711e06fa95546e1a9629b63de3aaae85fac9dc752fb533f3e5be23'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18rc1.linux-armv6l.tar.gz'; 			sha256='d7a3f97b23b1e1f2e1a3596ff011e78f93aa8bbd991e2065ac34c18993884ea1'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18rc1.linux-arm64.tar.gz'; 			sha256='e4528a113016872a3715cec37a6c6dad36d76d51a50fa19b33b7673e47e6df44'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18rc1.linux-386.tar.gz'; 			sha256='a4bb0097276fa3523f1ce84dc4ee50fab0b3b0f7fbe72833710434889516c51e'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18rc1.linux-ppc64le.tar.gz'; 			sha256='a2944dfc3ee22efe1b940f122ee36cb4bb446e209116e5e8f244e78682ece981'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18rc1.linux-s390x.tar.gz'; 			sha256='e5578b8cbcc90659496f3930c61c6974c039d32d0573a6726c5d8e62f7e42d68'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18rc1.src.tar.gz'; 		sha256='5cec7a6653008fa85f8821b33665de37be289b7a02f17f36f705a88c43980bb8'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 18 Feb 2022 04:21:31 GMT
ENV GOPATH=/go
# Fri, 18 Feb 2022 04:21:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Feb 2022 04:21:33 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 18 Feb 2022 04:21:33 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:046501ac4c58f014cc320324f6023bbef17f28025428833449198a62a97849c0`  
		Last Modified: Wed, 26 Jan 2022 01:57:13 GMT  
		Size: 50.1 MB (50117358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29bf76217944d3c3b29fb3234ed71ba5a004ffcec0595d3704c6e6cfa169b68`  
		Last Modified: Wed, 26 Jan 2022 17:03:48 GMT  
		Size: 4.9 MB (4922334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce0e88eaa9f33e97d48fa77ed2c178123150031494073f10c97755b3bd6370c1`  
		Last Modified: Wed, 26 Jan 2022 17:03:50 GMT  
		Size: 10.2 MB (10216891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9436ef0f28d4835e8f606ab54b1c3982ebba4b0ea19b88e655a8c5c2e973c46`  
		Last Modified: Wed, 26 Jan 2022 17:04:41 GMT  
		Size: 50.3 MB (50327864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24126aa02d6fd7694a9ee89072fac017f1c227aaa47dfe47129ff1f52a5a00f`  
		Last Modified: Thu, 27 Jan 2022 20:48:20 GMT  
		Size: 64.8 MB (64761890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49affb90f93da522f3e546da5e43a2ba80359fbb40a8b9f4e90d75e00e69078`  
		Last Modified: Fri, 18 Feb 2022 04:59:38 GMT  
		Size: 110.0 MB (109975847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae2ec62a6d5a30b4c4eea6ee92ed816dd740c4983e4a0a6fb19a327b5811b87`  
		Last Modified: Fri, 18 Feb 2022 04:58:27 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:d5b76093afa2466271714fc6b9add986c8b9a5a1b50f3231cfd3aa48315e2a99
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.7 MB (313721436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b101d31cb6201d290b2963008e03cc3220d93888c5db8f916f65bac0a6cdbc1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:12 GMT
ADD file:9d66afa8fc90803d689e087b38b38a3bd58d0434b495ca4165ca520e73bccf55 in / 
# Tue, 01 Mar 2022 02:11:14 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:33:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:34:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 10:34:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 06:55:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 06:55:56 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Mar 2022 06:55:57 GMT
ENV GOLANG_VERSION=1.18rc1
# Wed, 02 Mar 2022 06:57:15 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18rc1.linux-amd64.tar.gz'; 			sha256='9ea4e6adee711e06fa95546e1a9629b63de3aaae85fac9dc752fb533f3e5be23'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18rc1.linux-armv6l.tar.gz'; 			sha256='d7a3f97b23b1e1f2e1a3596ff011e78f93aa8bbd991e2065ac34c18993884ea1'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18rc1.linux-arm64.tar.gz'; 			sha256='e4528a113016872a3715cec37a6c6dad36d76d51a50fa19b33b7673e47e6df44'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18rc1.linux-386.tar.gz'; 			sha256='a4bb0097276fa3523f1ce84dc4ee50fab0b3b0f7fbe72833710434889516c51e'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18rc1.linux-ppc64le.tar.gz'; 			sha256='a2944dfc3ee22efe1b940f122ee36cb4bb446e209116e5e8f244e78682ece981'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18rc1.linux-s390x.tar.gz'; 			sha256='e5578b8cbcc90659496f3930c61c6974c039d32d0573a6726c5d8e62f7e42d68'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18rc1.src.tar.gz'; 		sha256='5cec7a6653008fa85f8821b33665de37be289b7a02f17f36f705a88c43980bb8'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 02 Mar 2022 06:57:16 GMT
ENV GOPATH=/go
# Wed, 02 Mar 2022 06:57:17 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Mar 2022 06:57:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 02 Mar 2022 06:57:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c7869242ae9abf6340558e18846f64a05eb06f2eaf66c6bfa2dc66ff2c997976`  
		Last Modified: Tue, 01 Mar 2022 02:17:52 GMT  
		Size: 53.6 MB (53608753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9880592b351f34fa791bd7749a127063cd6a76b1190bd059c168696d700f6b04`  
		Last Modified: Tue, 01 Mar 2022 10:44:26 GMT  
		Size: 5.1 MB (5141642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd9934a374f1ba93d2da0983d2aac86c9b4bf6ca063aa108519d2588e0212ac`  
		Last Modified: Tue, 01 Mar 2022 10:44:26 GMT  
		Size: 10.7 MB (10655864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37be3698694527b9e5af78494bbcb68f6b045af5247de8c988b24ef7dcd877e`  
		Last Modified: Tue, 01 Mar 2022 10:44:48 GMT  
		Size: 54.7 MB (54671139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de0634a187f2a5eafe92e5c690219dc718710435d988d4ba609487163ae4b01`  
		Last Modified: Wed, 02 Mar 2022 07:11:08 GMT  
		Size: 81.0 MB (81021300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b488fcc46fef88eacbd705235eb785ed9908bc42a85f17183fbb89973886fcb7`  
		Last Modified: Wed, 02 Mar 2022 07:11:13 GMT  
		Size: 108.6 MB (108622612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f68eb2a472dc18f8763f1b1342f97fff876402919a1c88aaa70c20b6db6c5b47`  
		Last Modified: Wed, 02 Mar 2022 07:10:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-bullseye` - linux; 386

```console
$ docker pull golang@sha256:b0be0f3652045737a9380866e32487e7c7ee1ab7273b2926c0979b151942c82c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.4 MB (328441764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0ea8ba38097670cc794ab755f51613e1755f4b52632c1413012025d0702361`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:07:15 GMT
ADD file:4341f64e7f1accc7f9737a9896bf50c6ba8f51698e52c594d9421fe4f2374e2a in / 
# Tue, 01 Mar 2022 02:07:15 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 05:40:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:41:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 05:41:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 04:37:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 04:37:26 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Mar 2022 04:37:26 GMT
ENV GOLANG_VERSION=1.18rc1
# Wed, 02 Mar 2022 04:38:57 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18rc1.linux-amd64.tar.gz'; 			sha256='9ea4e6adee711e06fa95546e1a9629b63de3aaae85fac9dc752fb533f3e5be23'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18rc1.linux-armv6l.tar.gz'; 			sha256='d7a3f97b23b1e1f2e1a3596ff011e78f93aa8bbd991e2065ac34c18993884ea1'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18rc1.linux-arm64.tar.gz'; 			sha256='e4528a113016872a3715cec37a6c6dad36d76d51a50fa19b33b7673e47e6df44'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18rc1.linux-386.tar.gz'; 			sha256='a4bb0097276fa3523f1ce84dc4ee50fab0b3b0f7fbe72833710434889516c51e'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18rc1.linux-ppc64le.tar.gz'; 			sha256='a2944dfc3ee22efe1b940f122ee36cb4bb446e209116e5e8f244e78682ece981'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18rc1.linux-s390x.tar.gz'; 			sha256='e5578b8cbcc90659496f3930c61c6974c039d32d0573a6726c5d8e62f7e42d68'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18rc1.src.tar.gz'; 		sha256='5cec7a6653008fa85f8821b33665de37be289b7a02f17f36f705a88c43980bb8'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 02 Mar 2022 04:38:58 GMT
ENV GOPATH=/go
# Wed, 02 Mar 2022 04:38:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Mar 2022 04:38:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 02 Mar 2022 04:38:59 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5cf8159e9217c5f37fe58b260cacc1d132c2e21ca58c769d29c6eb720993a304`  
		Last Modified: Tue, 01 Mar 2022 02:15:15 GMT  
		Size: 55.9 MB (55938747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1700db29f99e559f6f1909315637ddbda6667a35bd437b9e5d8c3beb373c6c1f`  
		Last Modified: Tue, 01 Mar 2022 05:51:55 GMT  
		Size: 5.3 MB (5283081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff041f2862924d1932eb1f5d7b01079bf8015dcc0dbb94a23d2475b8684d875a`  
		Last Modified: Tue, 01 Mar 2022 05:51:56 GMT  
		Size: 11.3 MB (11250640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ec658b51a80445b805d19e0462b4112f90132f61a78d8d7f5b29f6903e1e44`  
		Last Modified: Tue, 01 Mar 2022 05:52:25 GMT  
		Size: 55.9 MB (55919550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b4c03e566323e31b26438b87170c8b4fc3017bc855f2fbe0ebc948948e32e8a`  
		Last Modified: Wed, 02 Mar 2022 04:54:47 GMT  
		Size: 87.3 MB (87256982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2658001425ed8babe334eca64a9c1d65da06bcd3268543c011ca83a8c5ccb13`  
		Last Modified: Wed, 02 Mar 2022 04:54:51 GMT  
		Size: 112.8 MB (112792608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7092123e685eaf9a64a9ef2fedb2ebba3bc4e4b48c9788ef22f8bc3bca9c07ca`  
		Last Modified: Wed, 02 Mar 2022 04:54:12 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-bullseye` - linux; mips64le

```console
$ docker pull golang@sha256:1294c20adf18469e97c08a9dd68144deb3de9423eb40a0344b92b3bbc2ddb244
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298221116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf53a193d1884ce41174e2fecf5363aa4ab688f9d32e16e42966395b1cf930c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:42:19 GMT
ADD file:06fbff49d105bbaefb6199ecf549660a67db6cec16698f03c8ae0cf2bdfd6d4f in / 
# Wed, 26 Jan 2022 01:42:20 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 02:20:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 02:21:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 02:22:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 14:19:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 14:19:55 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Feb 2022 23:23:31 GMT
ENV GOLANG_VERSION=1.18rc1
# Thu, 17 Feb 2022 23:34:39 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18rc1.linux-amd64.tar.gz'; 			sha256='9ea4e6adee711e06fa95546e1a9629b63de3aaae85fac9dc752fb533f3e5be23'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18rc1.linux-armv6l.tar.gz'; 			sha256='d7a3f97b23b1e1f2e1a3596ff011e78f93aa8bbd991e2065ac34c18993884ea1'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18rc1.linux-arm64.tar.gz'; 			sha256='e4528a113016872a3715cec37a6c6dad36d76d51a50fa19b33b7673e47e6df44'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18rc1.linux-386.tar.gz'; 			sha256='a4bb0097276fa3523f1ce84dc4ee50fab0b3b0f7fbe72833710434889516c51e'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18rc1.linux-ppc64le.tar.gz'; 			sha256='a2944dfc3ee22efe1b940f122ee36cb4bb446e209116e5e8f244e78682ece981'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18rc1.linux-s390x.tar.gz'; 			sha256='e5578b8cbcc90659496f3930c61c6974c039d32d0573a6726c5d8e62f7e42d68'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18rc1.src.tar.gz'; 		sha256='5cec7a6653008fa85f8821b33665de37be289b7a02f17f36f705a88c43980bb8'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 17 Feb 2022 23:34:41 GMT
ENV GOPATH=/go
# Thu, 17 Feb 2022 23:34:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Feb 2022 23:34:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 17 Feb 2022 23:34:44 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6176f4ee4b1d3ab7c5f3f93bc9036b71aa337a53c743b4aa347dffebfc8c772a`  
		Last Modified: Wed, 26 Jan 2022 01:50:39 GMT  
		Size: 53.2 MB (53179965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95348eb2d40b4ceb8a78cd0f25deda3892c77ac31efd5b0650b8d374354d6b4a`  
		Last Modified: Wed, 26 Jan 2022 02:37:45 GMT  
		Size: 5.1 MB (5114720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea6c8e8b27ca91be5bb90346420cd2dbf8981731b5c3b1a8a6fb3ec3df2f7b9`  
		Last Modified: Wed, 26 Jan 2022 02:37:48 GMT  
		Size: 10.9 MB (10873345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980b5119331280a76055ea16321d5b3844830fef6044f2fbe60f8f5938357a7c`  
		Last Modified: Wed, 26 Jan 2022 02:38:39 GMT  
		Size: 53.3 MB (53295729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a616f514c70e08a1a9920b20b4a83bcd3e505100a1ce3668b544370709adf4d1`  
		Last Modified: Thu, 27 Jan 2022 15:21:39 GMT  
		Size: 66.9 MB (66931941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d0320c67177bac084d78e268d6ded5fc81aa9ab672170e41ef9656103fbdba`  
		Last Modified: Fri, 18 Feb 2022 00:24:21 GMT  
		Size: 108.8 MB (108825291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65afc658c93fdccf9deac8909e92fc6a4926307e8c24f5dc3b8639187255c0cb`  
		Last Modified: Fri, 18 Feb 2022 00:23:06 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-bullseye` - linux; ppc64le

```console
$ docker pull golang@sha256:a9147a72876fed818ae2a8813fee908c8c9af76c02f1ead98d22dc7c14554711
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.8 MB (323806823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a20e29f7e953cf8410b6421b3aab0a2737c60a4d65c35619cea6238bc42bbd4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:04:22 GMT
ADD file:00554eaeb433a7cc43c22f2544d800896f451a2e5a7895863c4651ed425b8c36 in / 
# Tue, 01 Mar 2022 02:04:29 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 07:06:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 07:07:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 07:09:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 17:00:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 17:00:20 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 17:00:23 GMT
ENV GOLANG_VERSION=1.18rc1
# Tue, 01 Mar 2022 17:01:46 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18rc1.linux-amd64.tar.gz'; 			sha256='9ea4e6adee711e06fa95546e1a9629b63de3aaae85fac9dc752fb533f3e5be23'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18rc1.linux-armv6l.tar.gz'; 			sha256='d7a3f97b23b1e1f2e1a3596ff011e78f93aa8bbd991e2065ac34c18993884ea1'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18rc1.linux-arm64.tar.gz'; 			sha256='e4528a113016872a3715cec37a6c6dad36d76d51a50fa19b33b7673e47e6df44'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18rc1.linux-386.tar.gz'; 			sha256='a4bb0097276fa3523f1ce84dc4ee50fab0b3b0f7fbe72833710434889516c51e'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18rc1.linux-ppc64le.tar.gz'; 			sha256='a2944dfc3ee22efe1b940f122ee36cb4bb446e209116e5e8f244e78682ece981'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18rc1.linux-s390x.tar.gz'; 			sha256='e5578b8cbcc90659496f3930c61c6974c039d32d0573a6726c5d8e62f7e42d68'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18rc1.src.tar.gz'; 		sha256='5cec7a6653008fa85f8821b33665de37be289b7a02f17f36f705a88c43980bb8'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Tue, 01 Mar 2022 17:01:55 GMT
ENV GOPATH=/go
# Tue, 01 Mar 2022 17:01:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 17:02:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 01 Mar 2022 17:02:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9ff352265b4a055377b95db6dddea03717bbefbc7f30fbacf493764d617ae85e`  
		Last Modified: Tue, 01 Mar 2022 02:14:41 GMT  
		Size: 58.8 MB (58834115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c6e10a400e162a4b996dd3e9c41cf812cfdb85d9830543b1c0b42305ab08b61`  
		Last Modified: Tue, 01 Mar 2022 07:42:05 GMT  
		Size: 5.4 MB (5401790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7ac604ebf8c0f6690f9477f7cba586130342d01fb167fc710f6621475e1786`  
		Last Modified: Tue, 01 Mar 2022 07:42:06 GMT  
		Size: 11.6 MB (11625870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20dd043e4a99bc0c4d1ed0c5ead9dcddb30bb43c85f40f573a87b12292f70b4`  
		Last Modified: Tue, 01 Mar 2022 07:42:32 GMT  
		Size: 58.9 MB (58854072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b9e7f99efef65249e101d28baa4f3b95cebd217c0146ca2b143e2640b9549e1`  
		Last Modified: Tue, 01 Mar 2022 17:34:19 GMT  
		Size: 80.3 MB (80288088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e36619acdc3e924f50f54bbd04b742cd73540e1a102be23a91c4cc59d9ae2e`  
		Last Modified: Tue, 01 Mar 2022 17:34:22 GMT  
		Size: 108.8 MB (108802732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49b9895e9e78d24de00fcbb0552b7b4ca70f37887dbf612cdd203c1eb8117ce`  
		Last Modified: Tue, 01 Mar 2022 17:34:04 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-bullseye` - linux; s390x

```console
$ docker pull golang@sha256:da7fa6497d9bfbb87e8a54ca14612ec3e7b0427a9b6aa7004c1581b305bc2f40
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.2 MB (300198087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80db124621d6ecf55a6a30fbb264d1a868d87cdeae67094abc1f455571ab2c19`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:01:38 GMT
ADD file:78e3de91b973a84a5cd4a6bfc7d75b5ce2e2ce578ab10784afb8e0c7f7c507f1 in / 
# Tue, 01 Mar 2022 02:01:41 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 03:51:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 03:51:29 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 03:51:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 15:41:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 15:41:55 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 15:41:55 GMT
ENV GOLANG_VERSION=1.18rc1
# Tue, 01 Mar 2022 15:43:19 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18rc1.linux-amd64.tar.gz'; 			sha256='9ea4e6adee711e06fa95546e1a9629b63de3aaae85fac9dc752fb533f3e5be23'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18rc1.linux-armv6l.tar.gz'; 			sha256='d7a3f97b23b1e1f2e1a3596ff011e78f93aa8bbd991e2065ac34c18993884ea1'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18rc1.linux-arm64.tar.gz'; 			sha256='e4528a113016872a3715cec37a6c6dad36d76d51a50fa19b33b7673e47e6df44'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18rc1.linux-386.tar.gz'; 			sha256='a4bb0097276fa3523f1ce84dc4ee50fab0b3b0f7fbe72833710434889516c51e'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18rc1.linux-ppc64le.tar.gz'; 			sha256='a2944dfc3ee22efe1b940f122ee36cb4bb446e209116e5e8f244e78682ece981'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18rc1.linux-s390x.tar.gz'; 			sha256='e5578b8cbcc90659496f3930c61c6974c039d32d0573a6726c5d8e62f7e42d68'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18rc1.src.tar.gz'; 		sha256='5cec7a6653008fa85f8821b33665de37be289b7a02f17f36f705a88c43980bb8'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Tue, 01 Mar 2022 15:43:23 GMT
ENV GOPATH=/go
# Tue, 01 Mar 2022 15:43:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 15:43:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 01 Mar 2022 15:43:24 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8414b15e1ad8e064415f8ebab6583f426769cd23e60d3c2a657521af0684754f`  
		Last Modified: Tue, 01 Mar 2022 02:07:14 GMT  
		Size: 53.2 MB (53210621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42eef690536ae738c85755ada1ea2f523244263a5b13f0493896d0d599ac66dc`  
		Last Modified: Tue, 01 Mar 2022 03:59:58 GMT  
		Size: 5.1 MB (5137006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb00ce32e18f4c73ceb3443995d23eb3d069c1ad6e091a9b864c43df543e99d9`  
		Last Modified: Tue, 01 Mar 2022 03:59:58 GMT  
		Size: 10.8 MB (10761280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d698cc9591dd8065c36ceaf2ab82adcaf9e1d56e33fdab4c8d0ae73448ab7f2`  
		Last Modified: Tue, 01 Mar 2022 04:00:14 GMT  
		Size: 54.0 MB (54044054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4c40fc2e42fc21d21969e3587194a9f1dba24943e0dfd443139571c3251bef`  
		Last Modified: Tue, 01 Mar 2022 15:54:19 GMT  
		Size: 65.5 MB (65539209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb2e1ad9c60426220f92aaacd72e67cd9877604497125e663f418c2c1e7b515`  
		Last Modified: Tue, 01 Mar 2022 15:54:24 GMT  
		Size: 111.5 MB (111505762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b1e2bfb872cf3ba19bf5b8111627e090be59e1e2667d3956d0af29880060f8`  
		Last Modified: Tue, 01 Mar 2022 15:54:11 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
