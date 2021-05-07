## `golang:latest`

```console
$ docker pull golang@sha256:07a471a939cd942ed5c23714185dac476df214f94cf073ef2fbfa748d4926a48
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
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `golang:latest` - linux; amd64

```console
$ docker pull golang@sha256:8f7c5b9000f0531bb28860dc1232ca0defa346361e2003dbf324982407cfe927
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.9 MB (317885619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4904add04a6c4e5cf43225f41f2eb0e27e9830e6c0f0f363232593b0b0fc44`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 10 Apr 2021 01:20:08 GMT
ADD file:e18bc3e10e7c743f18bb8be65ec94a62c03764af7dbdb4957f9a600237730212 in / 
# Sat, 10 Apr 2021 01:20:09 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:54:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 01:54:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 10 Apr 2021 01:54:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sun, 11 Apr 2021 00:22:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Sun, 11 Apr 2021 00:22:06 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:17:24 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 23:17:37 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.16.4.linux-amd64.tar.gz'; 			sha256='7154e88f5a8047aad4b80ebace58a059e36e7e2e4eb3b383127a28c711b4ff59'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.16.4.linux-armv6l.tar.gz'; 			sha256='a53391a800ddec749ee90d38992babb27b95cfb864027350c737b9aa8e069494'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.16.4.linux-arm64.tar.gz'; 			sha256='8b18eb05ddda2652d69ab1b1dd1f40dd731799f43c6a58b512ad01ae5b5bba21'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.16.4.linux-386.tar.gz'; 			sha256='cd1b146ef6e9006f27dd99e9687773e7fef30e8c985b7d41bff33e955a3bb53a'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.16.4.linux-ppc64le.tar.gz'; 			sha256='80cfac566e344096a8df8f37bbd21f89e76a6fbe601406565d71a87a665fc125'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.16.4.linux-s390x.tar.gz'; 			sha256='d6431881b3573dc29ecc24fbeab5e5ec25d8c9273aa543769c86a1a3bbac1ddf'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 		sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 06 May 2021 23:17:38 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 23:17:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:17:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 23:17:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bd8f6a7501ccbe80b95c82519ed6fd4f7236a41e0ae59ba4a8df76af24629efc`  
		Last Modified: Sat, 10 Apr 2021 01:24:48 GMT  
		Size: 50.4 MB (50432971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44718e6d535d365250316b02459f98a1b0fa490158cc53057d18858507504d60`  
		Last Modified: Sat, 10 Apr 2021 02:01:57 GMT  
		Size: 7.8 MB (7832944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe9738af0cb2184ee8f3fb3dcb130455385aa428a27d14e1e07a5587ff16e64`  
		Last Modified: Sat, 10 Apr 2021 02:01:59 GMT  
		Size: 10.0 MB (9997183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37aabde37b87d272286df45e6a3145b0884b72e07e657bf1a2a1e74a92c6172`  
		Last Modified: Sat, 10 Apr 2021 02:02:22 GMT  
		Size: 51.8 MB (51841093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c446e03742436a63658a4694134a27c8fd15833ed35c62997a1fd7bb87c500`  
		Last Modified: Sun, 11 Apr 2021 00:24:31 GMT  
		Size: 68.7 MB (68736458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce42924a962dcc27fe0bac5beecfe3051f3ffcbba89bb39d632712210cb909b`  
		Last Modified: Thu, 06 May 2021 23:28:28 GMT  
		Size: 129.0 MB (129044813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1de2e1f70784cb8bd3b6e25b0250b13f7d90432baed9fc37e05febf068e8a72`  
		Last Modified: Thu, 06 May 2021 23:28:05 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - linux; arm variant v5

```console
$ docker pull golang@sha256:2a54f92b967e208fe9ada5bf3a1de7d8b234b58288feecd548822917e52046bf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269385201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55a8631cbed018bdc1eb178cb77187a649bcd1d85e7a8dac4018dc60be9f61f2`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 10 Apr 2021 00:51:03 GMT
ADD file:1b971030610d93168a72e3a82bac2d23dfaf0519be9b0cd24596e21761ce3837 in / 
# Sat, 10 Apr 2021 00:51:07 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 02:02:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 02:03:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 10 Apr 2021 02:04:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 11:57:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 11:57:31 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 21:32:51 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 21:36:29 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.16.4.linux-amd64.tar.gz'; 			sha256='7154e88f5a8047aad4b80ebace58a059e36e7e2e4eb3b383127a28c711b4ff59'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.16.4.linux-armv6l.tar.gz'; 			sha256='a53391a800ddec749ee90d38992babb27b95cfb864027350c737b9aa8e069494'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.16.4.linux-arm64.tar.gz'; 			sha256='8b18eb05ddda2652d69ab1b1dd1f40dd731799f43c6a58b512ad01ae5b5bba21'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.16.4.linux-386.tar.gz'; 			sha256='cd1b146ef6e9006f27dd99e9687773e7fef30e8c985b7d41bff33e955a3bb53a'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.16.4.linux-ppc64le.tar.gz'; 			sha256='80cfac566e344096a8df8f37bbd21f89e76a6fbe601406565d71a87a665fc125'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.16.4.linux-s390x.tar.gz'; 			sha256='d6431881b3573dc29ecc24fbeab5e5ec25d8c9273aa543769c86a1a3bbac1ddf'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 		sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 06 May 2021 21:36:38 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 21:36:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 21:36:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 21:36:43 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3c06faee41008db891ee3639eb45f5703ab8b865e7ed637997d6f9f9549ac0ef`  
		Last Modified: Sat, 10 Apr 2021 00:58:59 GMT  
		Size: 48.1 MB (48149130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3cbc9c29f2277dd77644c394d167227ced2c7f34300a31a383eaecd0bce22f`  
		Last Modified: Sat, 10 Apr 2021 02:19:00 GMT  
		Size: 7.4 MB (7376533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d381d109c0d0c28597405dae6e0dad96a189bb700571bea48863c242c56f59`  
		Last Modified: Sat, 10 Apr 2021 02:19:01 GMT  
		Size: 9.7 MB (9687553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7310d88e88f65f721330cf40b3f791383dc06d5855e03f2cf9a9b31d226b4521`  
		Last Modified: Sat, 10 Apr 2021 02:19:29 GMT  
		Size: 49.6 MB (49574896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8720872f7d7182dc47c425e3d6c1fea34a5fb7f50553aff18fed19af042f7af2`  
		Last Modified: Sat, 10 Apr 2021 12:15:26 GMT  
		Size: 52.0 MB (52041739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba4a9cc65aaddbbb02039417c34e713a3aa6b0fbf7b5493e0c15dd9fe68af0e`  
		Last Modified: Thu, 06 May 2021 21:41:12 GMT  
		Size: 102.6 MB (102555196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d140de78189f201d39eed2fe64eee0166145b81ac189bc1e7d0584e69883503a`  
		Last Modified: Thu, 06 May 2021 21:40:41 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - linux; arm variant v7

```console
$ docker pull golang@sha256:e06bce036587aff6a7a07e6dd928d4f523ebd3531e327474bc35c5595606f325
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263242410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:459168424042633748736898c865080a4672c25cd2c90c1b8b669a2ac91401ed`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 10 Apr 2021 00:59:18 GMT
ADD file:bd2081229497eea2b33310cb1582b965581ca78b00b87cc8e42bdc8b9f350678 in / 
# Sat, 10 Apr 2021 00:59:20 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 06:05:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 06:05:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 10 Apr 2021 06:06:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 22:21:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 22:21:38 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:10:16 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 23:10:42 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.16.4.linux-amd64.tar.gz'; 			sha256='7154e88f5a8047aad4b80ebace58a059e36e7e2e4eb3b383127a28c711b4ff59'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.16.4.linux-armv6l.tar.gz'; 			sha256='a53391a800ddec749ee90d38992babb27b95cfb864027350c737b9aa8e069494'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.16.4.linux-arm64.tar.gz'; 			sha256='8b18eb05ddda2652d69ab1b1dd1f40dd731799f43c6a58b512ad01ae5b5bba21'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.16.4.linux-386.tar.gz'; 			sha256='cd1b146ef6e9006f27dd99e9687773e7fef30e8c985b7d41bff33e955a3bb53a'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.16.4.linux-ppc64le.tar.gz'; 			sha256='80cfac566e344096a8df8f37bbd21f89e76a6fbe601406565d71a87a665fc125'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.16.4.linux-s390x.tar.gz'; 			sha256='d6431881b3573dc29ecc24fbeab5e5ec25d8c9273aa543769c86a1a3bbac1ddf'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 		sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 06 May 2021 23:10:43 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 23:10:44 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:10:47 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 23:10:48 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:de0ca59eb81518ffd92fbcd386251018f950dc16b1bd8ad2e642184db76be2a1`  
		Last Modified: Sat, 10 Apr 2021 01:07:26 GMT  
		Size: 45.9 MB (45915598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed23bfa8aaeab64a1ca00d3bead680f790be28326d14305705b2ee5227b4f2b7`  
		Last Modified: Sat, 10 Apr 2021 06:19:54 GMT  
		Size: 7.1 MB (7124181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a12824e68a5072613049fad15fc8f0d209526ddd9d85787cc60d1b0d5073c0`  
		Last Modified: Sat, 10 Apr 2021 06:19:55 GMT  
		Size: 9.3 MB (9343784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da73a12ad465a34e484807c20e78927bd0dbd29a487e06024dbf3a1e21ba8a39`  
		Last Modified: Sat, 10 Apr 2021 06:20:19 GMT  
		Size: 47.4 MB (47356313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2edff18c3f8654da2fb892bb50883c5f5f205d704da1723f1d4e6d8a2bc8042`  
		Last Modified: Sat, 10 Apr 2021 22:26:19 GMT  
		Size: 53.2 MB (53205297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb8b88fb64d348f3f4dd931bf4caf3609457111afe81f1c56bbd8bf7931ec82`  
		Last Modified: Thu, 06 May 2021 23:26:56 GMT  
		Size: 100.3 MB (100297080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15aa19efd20cdbc39074a0fb7867da0edebda2b6a84e9f1b188a52c1b8c842f`  
		Last Modified: Thu, 06 May 2021 23:26:27 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:7037a153b6e0449133cbcd9102bad745df35f85a05c70d4bdf3e63a3fa3078df
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281285432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b7ff64e9c7af7c971cb29e8cf125fe5c8449e3ed213c50837a3dc085a80a68`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 10 Apr 2021 00:40:59 GMT
ADD file:320ad0e2a3d6c676ddb8ce5646b5a94d18d82a8868955da3a9379a261dfe1ffe in / 
# Sat, 10 Apr 2021 00:41:01 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:46:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 01:46:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 10 Apr 2021 01:47:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 21:42:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 21:42:12 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 22:30:30 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 22:30:48 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.16.4.linux-amd64.tar.gz'; 			sha256='7154e88f5a8047aad4b80ebace58a059e36e7e2e4eb3b383127a28c711b4ff59'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.16.4.linux-armv6l.tar.gz'; 			sha256='a53391a800ddec749ee90d38992babb27b95cfb864027350c737b9aa8e069494'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.16.4.linux-arm64.tar.gz'; 			sha256='8b18eb05ddda2652d69ab1b1dd1f40dd731799f43c6a58b512ad01ae5b5bba21'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.16.4.linux-386.tar.gz'; 			sha256='cd1b146ef6e9006f27dd99e9687773e7fef30e8c985b7d41bff33e955a3bb53a'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.16.4.linux-ppc64le.tar.gz'; 			sha256='80cfac566e344096a8df8f37bbd21f89e76a6fbe601406565d71a87a665fc125'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.16.4.linux-s390x.tar.gz'; 			sha256='d6431881b3573dc29ecc24fbeab5e5ec25d8c9273aa543769c86a1a3bbac1ddf'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 		sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 06 May 2021 22:30:53 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 22:30:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 22:30:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 22:30:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:01cf0f0da10ede0eec0fc1c5fbfdeb63a447dfcc0a3c4419c0a4c3f0a2826636`  
		Last Modified: Sat, 10 Apr 2021 00:47:28 GMT  
		Size: 49.2 MB (49225782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c667eb56cd05909001c1c50e81cbc75e290fd8e353f974bab4246a0d4fc484ca`  
		Last Modified: Sat, 10 Apr 2021 02:01:00 GMT  
		Size: 7.7 MB (7695101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ca15a4cef673e0e1a7bc3e659f4653df9bce82b945e367475e436852cc7880`  
		Last Modified: Sat, 10 Apr 2021 02:00:59 GMT  
		Size: 10.0 MB (9984406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7f1cf823a7fca9771e278355d8924fac8d9cef1f8e3ecbc87332c4859d1d4f`  
		Last Modified: Sat, 10 Apr 2021 02:01:23 GMT  
		Size: 52.2 MB (52167974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:badf929bd8bb50d8e53c0eab7e09c081b2364f11af58c9928959f2f50994fb5f`  
		Last Modified: Sat, 10 Apr 2021 21:47:03 GMT  
		Size: 62.6 MB (62598426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba2f092ad24110f94a595bb0eca57c5bf84bc66df68563cce095f9f88725cf4`  
		Last Modified: Thu, 06 May 2021 22:43:09 GMT  
		Size: 99.6 MB (99613587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43de7b194ec5e91bbb7857de9a137c298d289a55918f7810fbdeb139bec2414`  
		Last Modified: Thu, 06 May 2021 22:42:42 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - linux; 386

```console
$ docker pull golang@sha256:c2cf9f996d8e8549155718d05027b0229264cc0a79212c3b4ce757644b07e96e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299663808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7fa8e8df1bbf3b225706c3763ebf1699bf66d99c3f67eab1700ad652b3239eb`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 10 Apr 2021 00:39:26 GMT
ADD file:de914d3ff1619f3af1574fb9644ffde6f0590dfcfe402ffc9e7b2c0500481706 in / 
# Sat, 10 Apr 2021 00:39:26 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 03:17:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 03:18:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 10 Apr 2021 03:18:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 16:30:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 16:30:35 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 22:17:55 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 22:18:20 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.16.4.linux-amd64.tar.gz'; 			sha256='7154e88f5a8047aad4b80ebace58a059e36e7e2e4eb3b383127a28c711b4ff59'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.16.4.linux-armv6l.tar.gz'; 			sha256='a53391a800ddec749ee90d38992babb27b95cfb864027350c737b9aa8e069494'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.16.4.linux-arm64.tar.gz'; 			sha256='8b18eb05ddda2652d69ab1b1dd1f40dd731799f43c6a58b512ad01ae5b5bba21'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.16.4.linux-386.tar.gz'; 			sha256='cd1b146ef6e9006f27dd99e9687773e7fef30e8c985b7d41bff33e955a3bb53a'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.16.4.linux-ppc64le.tar.gz'; 			sha256='80cfac566e344096a8df8f37bbd21f89e76a6fbe601406565d71a87a665fc125'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.16.4.linux-s390x.tar.gz'; 			sha256='d6431881b3573dc29ecc24fbeab5e5ec25d8c9273aa543769c86a1a3bbac1ddf'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 		sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 06 May 2021 22:18:21 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 22:18:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 22:18:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 22:18:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:848aed59cb94060ff383c5bac16a4d69d7babe251466ce3f80195bf8f7209702`  
		Last Modified: Sat, 10 Apr 2021 00:45:25 GMT  
		Size: 51.2 MB (51198915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a9a21c9b0223b401e8c30ae192393dc70df9e1a30c508b5ba60df0675625935`  
		Last Modified: Sat, 10 Apr 2021 03:29:57 GMT  
		Size: 8.0 MB (7998631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329fe24924003b4f394237227c62c24c2b7686dbd0b4cbe71f697f640abfce81`  
		Last Modified: Sat, 10 Apr 2021 03:29:57 GMT  
		Size: 10.3 MB (10339977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86ae4848eb15b935a836fa443b81da7ceb1176b6d679045f3a734272bfb1707d`  
		Last Modified: Sat, 10 Apr 2021 03:30:33 GMT  
		Size: 53.4 MB (53437928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02ff06f82bb68fa018829d7aab5e4b64813bd5c0980f3ad7b328e23b2bb7fc6`  
		Last Modified: Sat, 10 Apr 2021 16:35:03 GMT  
		Size: 73.6 MB (73597902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe9d2dfb8d1f6aad9ce40ebba68396432fb092255d63a9e0d40ce57ebabb4cb`  
		Last Modified: Thu, 06 May 2021 22:43:15 GMT  
		Size: 103.1 MB (103090300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2f0e91418a0133f7d8d4bd44d47fb735a7df5848929d5eedcc9132ff6a4522`  
		Last Modified: Thu, 06 May 2021 22:42:40 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - linux; mips64le

```console
$ docker pull golang@sha256:0f321f43d7124c49cf20a1b1a5709f91c745b82ac59250a02da8b2f70f43f617
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.5 MB (271457175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1aa6c7b0d41cca06066748a978882fae4f8a63c07a908927998012ac4d205f0`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 10 Apr 2021 01:09:16 GMT
ADD file:76d04de63b0abd4b467c1af49e65bf93f854f7a99965790bf5ae8a5d5d4eff52 in / 
# Sat, 10 Apr 2021 01:09:17 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 02:07:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 02:07:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 10 Apr 2021 02:08:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 15:56:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 15:56:33 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 20:48:10 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 20:56:01 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.16.4.linux-amd64.tar.gz'; 			sha256='7154e88f5a8047aad4b80ebace58a059e36e7e2e4eb3b383127a28c711b4ff59'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.16.4.linux-armv6l.tar.gz'; 			sha256='a53391a800ddec749ee90d38992babb27b95cfb864027350c737b9aa8e069494'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.16.4.linux-arm64.tar.gz'; 			sha256='8b18eb05ddda2652d69ab1b1dd1f40dd731799f43c6a58b512ad01ae5b5bba21'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.16.4.linux-386.tar.gz'; 			sha256='cd1b146ef6e9006f27dd99e9687773e7fef30e8c985b7d41bff33e955a3bb53a'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.16.4.linux-ppc64le.tar.gz'; 			sha256='80cfac566e344096a8df8f37bbd21f89e76a6fbe601406565d71a87a665fc125'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.16.4.linux-s390x.tar.gz'; 			sha256='d6431881b3573dc29ecc24fbeab5e5ec25d8c9273aa543769c86a1a3bbac1ddf'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 		sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 06 May 2021 20:56:02 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 20:56:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 20:56:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 20:56:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:437194c1aac057ffc15e81662666c0514263f66844c3fb685f8eb711c9b1d5b3`  
		Last Modified: Sat, 10 Apr 2021 01:15:20 GMT  
		Size: 49.1 MB (49081824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb75a7e91e7c3217150c14a2e864c3194b8d8fa134057032352db7e33215141`  
		Last Modified: Sat, 10 Apr 2021 02:18:48 GMT  
		Size: 7.3 MB (7252482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0a522cec664fdadd94fceaaa3083e5793143f1d6402669712f09e5c634a3be`  
		Last Modified: Sat, 10 Apr 2021 02:18:48 GMT  
		Size: 10.0 MB (10016374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f883e819b37d86e804f6ee7839bd1b05fdbd362fbc25fa493e45714b68135398`  
		Last Modified: Sat, 10 Apr 2021 02:19:40 GMT  
		Size: 50.8 MB (50845406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17dbe7c32b8256725aca60c9cdaa69ee63906c1c9082e546b627d7adbf9682f9`  
		Last Modified: Sat, 10 Apr 2021 16:13:22 GMT  
		Size: 54.7 MB (54651372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60f3d4667805e2ee066a8aa1fdd6ea3e2501c6e270390f56df9aa5dc27cc950`  
		Last Modified: Thu, 06 May 2021 21:05:11 GMT  
		Size: 99.6 MB (99609591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70cf3e8898e943d33886b1811f756b4b42d5efde66fdab1fb6762953e1d8ad23`  
		Last Modified: Thu, 06 May 2021 21:04:02 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - linux; ppc64le

```console
$ docker pull golang@sha256:766171d9d4c5f91ef3580f2fcf0b1dcd5d66c3bc17f83f8090aedfe3322042ab
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.4 MB (302372444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4df07076e293728d8be6e5dae364854eff5201db0d6f55729d3d613e6694323`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 10 Apr 2021 01:26:11 GMT
ADD file:0671a70f02e705f591888f40e87a43122cd95a6ead3df61becbc4a7fb1c7ec43 in / 
# Sat, 10 Apr 2021 01:26:21 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 02:24:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 02:25:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 10 Apr 2021 02:28:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 16:31:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 16:31:48 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 May 2021 00:20:58 GMT
ENV GOLANG_VERSION=1.16.4
# Fri, 07 May 2021 00:21:50 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.16.4.linux-amd64.tar.gz'; 			sha256='7154e88f5a8047aad4b80ebace58a059e36e7e2e4eb3b383127a28c711b4ff59'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.16.4.linux-armv6l.tar.gz'; 			sha256='a53391a800ddec749ee90d38992babb27b95cfb864027350c737b9aa8e069494'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.16.4.linux-arm64.tar.gz'; 			sha256='8b18eb05ddda2652d69ab1b1dd1f40dd731799f43c6a58b512ad01ae5b5bba21'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.16.4.linux-386.tar.gz'; 			sha256='cd1b146ef6e9006f27dd99e9687773e7fef30e8c985b7d41bff33e955a3bb53a'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.16.4.linux-ppc64le.tar.gz'; 			sha256='80cfac566e344096a8df8f37bbd21f89e76a6fbe601406565d71a87a665fc125'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.16.4.linux-s390x.tar.gz'; 			sha256='d6431881b3573dc29ecc24fbeab5e5ec25d8c9273aa543769c86a1a3bbac1ddf'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 		sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 07 May 2021 00:22:05 GMT
ENV GOPATH=/go
# Fri, 07 May 2021 00:22:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 May 2021 00:22:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 07 May 2021 00:22:33 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d018a28ea8249b332e6bce3cb93862d5b05dba493dbaf3531505ce3a3701001b`  
		Last Modified: Sat, 10 Apr 2021 01:33:24 GMT  
		Size: 54.2 MB (54179922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1d690a663e373c9e09abb435ea1b9002ad11e9118b98f27767951ec963437e`  
		Last Modified: Sat, 10 Apr 2021 03:04:29 GMT  
		Size: 8.3 MB (8271815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de29ad508d11980c81b06641138821d118c6de9064228c4ee33bfedd156acf15`  
		Last Modified: Sat, 10 Apr 2021 03:04:29 GMT  
		Size: 10.7 MB (10727718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b93e64fc4b56829740f482d15d41f6be2348195960f65820b5565f1a7e81b7df`  
		Last Modified: Sat, 10 Apr 2021 03:04:56 GMT  
		Size: 57.5 MB (57457359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12da6e707e1dac21f9674edb655d32f3ae517ef9546d99a29fe874f1cd0f03ba`  
		Last Modified: Sat, 10 Apr 2021 16:35:41 GMT  
		Size: 73.6 MB (73643442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe0e41702fd6438ce9b900448527900e4f2a252fef702564beed13c30b5ca2e`  
		Last Modified: Fri, 07 May 2021 00:40:58 GMT  
		Size: 98.1 MB (98092032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f860ec91453736983587a0c228af3f60ea4ab2f196c105dc60fe1afd5bc5db8e`  
		Last Modified: Fri, 07 May 2021 00:39:43 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - linux; s390x

```console
$ docker pull golang@sha256:d75ea289253587ec53b79bc9059e8d07f04080cd3f9936b4cf57a48ea466b2a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277687579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bddb7b1db32d70f23d1bf3c62c11fddbf6792b5cbeabdbada3157d4bbeb3b428`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 10 Apr 2021 00:42:07 GMT
ADD file:4df1e9998bf12ac6b068948127db30e29fdc3196e27d72adf972c6c1cc6ce2a0 in / 
# Sat, 10 Apr 2021 00:42:10 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:27:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 01:28:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 10 Apr 2021 01:28:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 11:51:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 11:51:24 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:15:31 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 23:16:10 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.16.4.linux-amd64.tar.gz'; 			sha256='7154e88f5a8047aad4b80ebace58a059e36e7e2e4eb3b383127a28c711b4ff59'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.16.4.linux-armv6l.tar.gz'; 			sha256='a53391a800ddec749ee90d38992babb27b95cfb864027350c737b9aa8e069494'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.16.4.linux-arm64.tar.gz'; 			sha256='8b18eb05ddda2652d69ab1b1dd1f40dd731799f43c6a58b512ad01ae5b5bba21'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.16.4.linux-386.tar.gz'; 			sha256='cd1b146ef6e9006f27dd99e9687773e7fef30e8c985b7d41bff33e955a3bb53a'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.16.4.linux-ppc64le.tar.gz'; 			sha256='80cfac566e344096a8df8f37bbd21f89e76a6fbe601406565d71a87a665fc125'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.16.4.linux-s390x.tar.gz'; 			sha256='d6431881b3573dc29ecc24fbeab5e5ec25d8c9273aa543769c86a1a3bbac1ddf'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 		sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 06 May 2021 23:16:24 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 23:16:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:16:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 23:16:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:03bd9fa68773b62afcbde0348c41cadd08d602d2731d955581cc322351e8be39`  
		Last Modified: Sat, 10 Apr 2021 00:45:31 GMT  
		Size: 49.0 MB (49000527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:462b0816104d88c29adf6ff712d656e5b8ac57f3dfb17fdcb1cb5d2090b85fad`  
		Last Modified: Sat, 10 Apr 2021 01:33:41 GMT  
		Size: 7.4 MB (7400505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e318693fbecdee6c86a20d06396ea273a6f98a120b3e5a91f973416800bcaac2`  
		Last Modified: Sat, 10 Apr 2021 01:33:41 GMT  
		Size: 9.9 MB (9883023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee83389c8b4e83fa875720df895d5659e47a3d1a138254412dd52760e56be38`  
		Last Modified: Sat, 10 Apr 2021 01:33:54 GMT  
		Size: 51.4 MB (51380124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9413bea160f56f7408cd46a9c5e6f5ffac8aac961f37c3d4d2ccb510937a0e03`  
		Last Modified: Sat, 10 Apr 2021 11:54:42 GMT  
		Size: 56.8 MB (56803641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4af200ce533ce22d7add88d7b03bd6ccfba856d58000da9d43e8250e1d80caf`  
		Last Modified: Thu, 06 May 2021 23:33:42 GMT  
		Size: 103.2 MB (103219604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd775bb39e2845775427a263967a96fb2d5937abaa53a978bec6922392eedb26`  
		Last Modified: Thu, 06 May 2021 23:33:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - windows version 10.0.17763.1879; amd64

```console
$ docker pull golang@sha256:49de8040d411a236c55b2ab14906ed5ff4b38ed031be330e89ad9d2ac1265f2a
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2639628021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb27978fc7e1988ccbdd5b2793cd0687e2730f502e1326d5314a39bc56e56e7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 12:30:33 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Apr 2021 12:30:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Apr 2021 12:30:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Apr 2021 12:30:37 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Apr 2021 12:31:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:31:57 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Apr 2021 12:32:38 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 06 May 2021 20:16:07 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 20:18:44 GMT
RUN $url = 'https://dl.google.com/go/go1.16.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'd40139b7ade8a3008e3240a6f86fe8f899a9c465c917e11dac8758af216f5eb0'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 06 May 2021 20:18:46 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac56922ba0ee0ac19bcae98f5fb4b7427d31ef3c709f27cfb2c785fd13a611c4`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1723430d5101a2d617d3dbf4bc2a121b3f4b4432105aa2941e1afab8f130b9`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2f4dc6e9a77d69a3d172368f4ae471b31c588d6201c2386e4ac62fd83faa16`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaea47861a9221a4f1e5750db237c619796c612756a5e75e2cb443b1731ae8a8`  
		Last Modified: Wed, 14 Apr 2021 12:58:01 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4be4ebd8eabefdb01f27dafad85e65289b95ca15591c14304c7792db99b54b`  
		Last Modified: Wed, 14 Apr 2021 12:58:35 GMT  
		Size: 30.2 MB (30155601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f66ae3738a83ea41b428b49261d4522d57df1617fbd1aa362d93f1e2802643`  
		Last Modified: Wed, 14 Apr 2021 12:57:58 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2108b314c24064a0c250f72017cc64b3bf68915655327728a267c98985a5ff7`  
		Last Modified: Wed, 14 Apr 2021 12:57:58 GMT  
		Size: 324.6 KB (324649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa51985154dd0edd95ef4cc022400dc16b657c4a75cb3ade3675c58d316d0101`  
		Last Modified: Thu, 06 May 2021 20:34:43 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26942e7cec550ceca0e7b0ef319dc3f732731719adfc676869678adce06d1193`  
		Last Modified: Thu, 06 May 2021 20:35:15 GMT  
		Size: 139.4 MB (139382398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e6b3adacda0d1c5092f48a23fa73f5bb807876cf3dcf7fd71632b48d8b1987`  
		Last Modified: Thu, 06 May 2021 20:34:43 GMT  
		Size: 1.6 KB (1598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - windows version 10.0.14393.4350; amd64

```console
$ docker pull golang@sha256:909caf384f2e6e81124f40a0a38ca45e0edce381e5173fc3bb1a648718fb614c
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5980367918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d77c9989c6dab039c2c48b56bed5be3cda2b7a58d9d6615788302e0678b8c1d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 12:35:34 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Apr 2021 12:35:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Apr 2021 12:35:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Apr 2021 12:35:38 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Apr 2021 12:38:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 12:38:02 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Apr 2021 12:39:34 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 06 May 2021 20:19:05 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 20:22:32 GMT
RUN $url = 'https://dl.google.com/go/go1.16.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'd40139b7ade8a3008e3240a6f86fe8f899a9c465c917e11dac8758af216f5eb0'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 06 May 2021 20:22:34 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3360763b706a564d93471b21a342ebbda7e047567cf1cbee82dd592ad33e0c`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a0f653700ac9b57cf3d694cc90107e3220fc678581d1e985219677733ce242`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a59d82702c225a2ca8cd2a5476122f55d8619eae959c9cb8323b68d70a2ed19`  
		Last Modified: Wed, 14 Apr 2021 12:59:06 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62435cd2b7652fc97ef3dc1a8968446f3f6e95f0ff1d6dcb176a3f0c2b14c2f8`  
		Last Modified: Wed, 14 Apr 2021 12:59:08 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d78a3a3d6cb25f55dc9d9947f7449a14717e6b787e49571a837e72b79334cf`  
		Last Modified: Wed, 14 Apr 2021 12:59:41 GMT  
		Size: 30.8 MB (30752513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b774a32e346c00e004abbbd7290530d0a3f3dfb11915be2b2fa73c402da6bdd`  
		Last Modified: Wed, 14 Apr 2021 12:59:03 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d153061f2f0d8ef33f71c4b9afd90899e21556e320d7103a8a9fb544c1cb521`  
		Last Modified: Wed, 14 Apr 2021 12:59:11 GMT  
		Size: 5.6 MB (5608025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c85bf3447935a123c186c94d58b02a7e89b566366ab0c7a20b57fbc9e453e1`  
		Last Modified: Thu, 06 May 2021 20:35:33 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7558c3fc6da1f41d9317a885b7d1d896986e9e4a81b6487a543b93ca372649cd`  
		Last Modified: Thu, 06 May 2021 20:36:08 GMT  
		Size: 149.1 MB (149112181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d97cea35310e2e19e356bf67efe44136adb4df53f744e6497511765af70f7e`  
		Last Modified: Thu, 06 May 2021 20:35:33 GMT  
		Size: 1.5 KB (1506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
