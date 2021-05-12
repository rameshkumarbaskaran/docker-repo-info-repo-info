## `golang:stretch`

```console
$ docker pull golang@sha256:55a71c3375eb4eeaf971639d1b8a1c70b04259be4844e4c8464010da74449f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `golang:stretch` - linux; amd64

```console
$ docker pull golang@sha256:82c5c185bfd74cc369effc7f717a6953a93a3d3849010d752251a3158c26583a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 MB (297669753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aa159770894845689589f1b08daff1cd8e27c456ffe1bd3cbf3cb1455b39e7f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 10 Apr 2021 01:21:41 GMT
ADD file:e3d37689e896a83d39040f2c95091ff88f3899b5b410dbf76908dd6c938b8cb5 in / 
# Sat, 10 Apr 2021 01:21:41 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:57:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 01:57:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 10 Apr 2021 01:57:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sun, 11 Apr 2021 00:22:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Sun, 11 Apr 2021 00:22:35 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:17:45 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 23:18:00 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.16.4.linux-amd64.tar.gz'; 			sha256='7154e88f5a8047aad4b80ebace58a059e36e7e2e4eb3b383127a28c711b4ff59'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.16.4.linux-armv6l.tar.gz'; 			sha256='a53391a800ddec749ee90d38992babb27b95cfb864027350c737b9aa8e069494'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.16.4.linux-arm64.tar.gz'; 			sha256='8b18eb05ddda2652d69ab1b1dd1f40dd731799f43c6a58b512ad01ae5b5bba21'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.16.4.linux-386.tar.gz'; 			sha256='cd1b146ef6e9006f27dd99e9687773e7fef30e8c985b7d41bff33e955a3bb53a'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.16.4.linux-ppc64le.tar.gz'; 			sha256='80cfac566e344096a8df8f37bbd21f89e76a6fbe601406565d71a87a665fc125'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.16.4.linux-s390x.tar.gz'; 			sha256='d6431881b3573dc29ecc24fbeab5e5ec25d8c9273aa543769c86a1a3bbac1ddf'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 		sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 06 May 2021 23:18:01 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 23:18:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:18:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 23:18:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:76b8ef87096fa726adbe8f073ef69bb5664bac19474c5cce4dd69e08a234903b`  
		Last Modified: Sat, 10 Apr 2021 01:27:52 GMT  
		Size: 45.4 MB (45380037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2bafe8a0f40509cc10249087268e66a662e437f10e9598a09abb5687038a57`  
		Last Modified: Sat, 10 Apr 2021 02:04:34 GMT  
		Size: 11.3 MB (11286411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b53ce1fd2746e8d2037f1b0b91ddea0cc7411eb3e5949fe10c0320aca8f7392b`  
		Last Modified: Sat, 10 Apr 2021 02:04:33 GMT  
		Size: 4.3 MB (4342420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a8c1bd5887cc4a89e1f286fed9ee31ce12dba9f6813cf14082ada3e9ab6f63`  
		Last Modified: Sat, 10 Apr 2021 02:04:55 GMT  
		Size: 49.8 MB (49786874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cbd73091f2f8808c784a1e124884e97dc1f098c3731f4315ed1452c8837a4b3`  
		Last Modified: Sun, 11 Apr 2021 00:25:14 GMT  
		Size: 57.8 MB (57829132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129c36247defcc9eb3c2a108ec3f317b6085420ab25eac979bf0cdf7fab4349d`  
		Last Modified: Thu, 06 May 2021 23:29:08 GMT  
		Size: 129.0 MB (129044724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1abafd42473d60b0df964e6c1234094bb4215f235b47c58e8642611c3cfc0ef`  
		Last Modified: Thu, 06 May 2021 23:28:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:stretch` - linux; arm variant v7

```console
$ docker pull golang@sha256:c48cb30dc30d854e565beab2818ddf5edbc0c1d3180ab3840f0c48db0f18b47f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.6 MB (248567680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b8ecfa3aa388ff7acfe295567db1467318c0b7af602c5d64267f8e6dbd1db9`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 10 Apr 2021 01:02:42 GMT
ADD file:4c101c517b88a8d25a4997ab4d938ea50aaa265c7f88a4e63edaaed37d89a288 in / 
# Sat, 10 Apr 2021 01:02:43 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 06:12:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 06:12:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 10 Apr 2021 06:13:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 22:22:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 22:22:49 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:11:01 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 23:11:27 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.16.4.linux-amd64.tar.gz'; 			sha256='7154e88f5a8047aad4b80ebace58a059e36e7e2e4eb3b383127a28c711b4ff59'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.16.4.linux-armv6l.tar.gz'; 			sha256='a53391a800ddec749ee90d38992babb27b95cfb864027350c737b9aa8e069494'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.16.4.linux-arm64.tar.gz'; 			sha256='8b18eb05ddda2652d69ab1b1dd1f40dd731799f43c6a58b512ad01ae5b5bba21'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.16.4.linux-386.tar.gz'; 			sha256='cd1b146ef6e9006f27dd99e9687773e7fef30e8c985b7d41bff33e955a3bb53a'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.16.4.linux-ppc64le.tar.gz'; 			sha256='80cfac566e344096a8df8f37bbd21f89e76a6fbe601406565d71a87a665fc125'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.16.4.linux-s390x.tar.gz'; 			sha256='d6431881b3573dc29ecc24fbeab5e5ec25d8c9273aa543769c86a1a3bbac1ddf'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 		sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 06 May 2021 23:11:29 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 23:11:30 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:11:33 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 23:11:38 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:533b099902e847172558070703785f6c70f0c6912fefcfd283f3b0e3ebc306c5`  
		Last Modified: Sat, 10 Apr 2021 01:10:12 GMT  
		Size: 42.1 MB (42120304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba1eda48434fdafc900e072c3d26755397eb33edd3403430befc06bf5ebfe0d`  
		Last Modified: Sat, 10 Apr 2021 06:22:42 GMT  
		Size: 9.9 MB (9939854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a436419ab83cc68fde8e9c3d51a90fcb8c9874db9093ff594532fd4f5f4e54b8`  
		Last Modified: Sat, 10 Apr 2021 06:22:40 GMT  
		Size: 3.9 MB (3921286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74799456f267bce926877994b8951d39cba1f44f7784ba0eabc57c0eaf514db7`  
		Last Modified: Sat, 10 Apr 2021 06:23:03 GMT  
		Size: 46.1 MB (46127498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78327977c1ea85eeefcbe3e401661c86a718c6ad6e83fa5d18a576beac33015`  
		Last Modified: Sat, 10 Apr 2021 22:27:03 GMT  
		Size: 46.2 MB (46161473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef6e426a3420d5c4d3abbcebbf28000e94c2f42b96ae924d18e6a0e214d1633`  
		Last Modified: Thu, 06 May 2021 23:27:42 GMT  
		Size: 100.3 MB (100297110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59bf7a3fdb3189d66c58e3b6de64083de55efcc772409fd855fe3d97253a160b`  
		Last Modified: Thu, 06 May 2021 23:27:06 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:stretch` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:b1bd5832b968fe56872ae88f381d2d64ebf76110c745d6705f13d22e533a98e1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.0 MB (254049337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2141fe6af75ecdde824b90f07821fa485f4402396308b42139313debd4ca828`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 10 Apr 2021 00:43:48 GMT
ADD file:64990d14743657dbcbe885739e43ac964a0239a63e4693e6401b0884ab96e09b in / 
# Sat, 10 Apr 2021 00:43:50 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:53:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 01:53:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 10 Apr 2021 01:54:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 21:43:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 21:43:13 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 22:31:05 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 22:31:24 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.16.4.linux-amd64.tar.gz'; 			sha256='7154e88f5a8047aad4b80ebace58a059e36e7e2e4eb3b383127a28c711b4ff59'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.16.4.linux-armv6l.tar.gz'; 			sha256='a53391a800ddec749ee90d38992babb27b95cfb864027350c737b9aa8e069494'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.16.4.linux-arm64.tar.gz'; 			sha256='8b18eb05ddda2652d69ab1b1dd1f40dd731799f43c6a58b512ad01ae5b5bba21'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.16.4.linux-386.tar.gz'; 			sha256='cd1b146ef6e9006f27dd99e9687773e7fef30e8c985b7d41bff33e955a3bb53a'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.16.4.linux-ppc64le.tar.gz'; 			sha256='80cfac566e344096a8df8f37bbd21f89e76a6fbe601406565d71a87a665fc125'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.16.4.linux-s390x.tar.gz'; 			sha256='d6431881b3573dc29ecc24fbeab5e5ec25d8c9273aa543769c86a1a3bbac1ddf'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 		sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 06 May 2021 22:31:27 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 22:31:28 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 22:31:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 22:31:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:30bd672115ff6f225cb98d2d7f1ed62feb72c2612297b2ac615e762e436c64ec`  
		Last Modified: Sat, 10 Apr 2021 00:49:51 GMT  
		Size: 43.2 MB (43177772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7d38e5813e5a59ee1d86fb1c7c8c344342d0ec418aa440509260354958f9ad`  
		Last Modified: Sat, 10 Apr 2021 02:03:48 GMT  
		Size: 10.2 MB (10200972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8ce7d8aff50ac8c0f7baa508791ea69df0fa3c7dac0ab9be8933ce3ef5b68a`  
		Last Modified: Sat, 10 Apr 2021 02:03:46 GMT  
		Size: 4.1 MB (4096630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cdea9792a283a7de201b23b519db14e33c4a69b73fab9ec56ed56967eb688fc`  
		Last Modified: Sat, 10 Apr 2021 02:04:09 GMT  
		Size: 47.7 MB (47735206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb2fe268a7f5f9375d3b11bba9b553c663f4c6f087fe607a004eab7d74c9a66`  
		Last Modified: Sat, 10 Apr 2021 21:47:37 GMT  
		Size: 49.2 MB (49224867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2767991e88e012ec49b6f9a1f5230a304d8cb0cefd9df3bf4ac2cecf7c40b94`  
		Last Modified: Thu, 06 May 2021 22:43:45 GMT  
		Size: 99.6 MB (99613735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40efbd2be240d4563a7b5996217216e0c2f64c50bd80406d864cb7c9f4363f29`  
		Last Modified: Thu, 06 May 2021 22:43:18 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:stretch` - linux; 386

```console
$ docker pull golang@sha256:fea95f4edef250824bc900614c5ca16d595110044cd1766783936d0e26108f18
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.7 MB (278711984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d23e1afbec6c7f031da7c96c6ca735bbb76d526abf4cf5cf9f18ec4e2586691e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 May 2021 00:41:41 GMT
ADD file:3b26e2f83a0edf42ea62d20102b47011ee41cd2ab349c9da7487f62ff21b8471 in / 
# Wed, 12 May 2021 00:41:42 GMT
CMD ["bash"]
# Wed, 12 May 2021 01:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 01:12:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 12 May 2021 01:13:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 17:28:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Wed, 12 May 2021 17:28:06 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 May 2021 17:28:06 GMT
ENV GOLANG_VERSION=1.16.4
# Wed, 12 May 2021 17:28:20 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.16.4.linux-amd64.tar.gz'; 			sha256='7154e88f5a8047aad4b80ebace58a059e36e7e2e4eb3b383127a28c711b4ff59'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.16.4.linux-armv6l.tar.gz'; 			sha256='a53391a800ddec749ee90d38992babb27b95cfb864027350c737b9aa8e069494'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.16.4.linux-arm64.tar.gz'; 			sha256='8b18eb05ddda2652d69ab1b1dd1f40dd731799f43c6a58b512ad01ae5b5bba21'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.16.4.linux-386.tar.gz'; 			sha256='cd1b146ef6e9006f27dd99e9687773e7fef30e8c985b7d41bff33e955a3bb53a'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.16.4.linux-ppc64le.tar.gz'; 			sha256='80cfac566e344096a8df8f37bbd21f89e76a6fbe601406565d71a87a665fc125'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.16.4.linux-s390x.tar.gz'; 			sha256='d6431881b3573dc29ecc24fbeab5e5ec25d8c9273aa543769c86a1a3bbac1ddf'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 		sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 12 May 2021 17:28:21 GMT
ENV GOPATH=/go
# Wed, 12 May 2021 17:28:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 May 2021 17:28:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 12 May 2021 17:28:22 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2a179d76df60628ca372acea241dbf24d4039a86b7dc2ba920d26f64bded15a1`  
		Last Modified: Wed, 12 May 2021 00:49:13 GMT  
		Size: 46.1 MB (46098744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c213a4df67666087b0cfaa22f4d76fa708476c4f91ee848daccd8e1a9059682c`  
		Last Modified: Wed, 12 May 2021 01:21:01 GMT  
		Size: 11.3 MB (11336498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59de6391225c2ff4beecde954f63e31d511a479130b1acd174707008a47f717c`  
		Last Modified: Wed, 12 May 2021 01:20:59 GMT  
		Size: 4.6 MB (4564986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ee2df560b159f574ac071d2b70c54debf87201c8f108268b51b7b83f0cb410`  
		Last Modified: Wed, 12 May 2021 01:21:25 GMT  
		Size: 51.3 MB (51265871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e58c622f93a90ae4341900f5fff1ea3fb9752f61cb1bcd4d9c0832b4afe3a2a3`  
		Last Modified: Wed, 12 May 2021 17:32:13 GMT  
		Size: 62.4 MB (62355469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d57cfef858a52f2a92a7ec8224bfbe9a214a7d02c0959c47fcc1a7eb9dbde6b`  
		Last Modified: Wed, 12 May 2021 17:32:24 GMT  
		Size: 103.1 MB (103090261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a963967e9d4f79a034c1d293cd9ebcb2b35675f92fa00785676e9078fd3862`  
		Last Modified: Wed, 12 May 2021 17:31:42 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
