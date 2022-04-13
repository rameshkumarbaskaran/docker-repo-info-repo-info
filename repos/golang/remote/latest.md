## `golang:latest`

```console
$ docker pull golang@sha256:3f0168c019343d7cc07bf2481e7b6555fbf2ebadfb01f9e77875da66439ba041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 10
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.20348.643; amd64
	-	windows version 10.0.17763.2803; amd64

### `golang:latest` - linux; amd64

```console
$ docker pull golang@sha256:ee752bc53c628ff789bacefb714cff721701042ffa9eb736f7b2ed4e9f2bdab6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.1 MB (353081484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df7abb7452ed820621fb16b9f978ae9294c1d44ac46041c9083f139b959ac96`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:07 GMT
ADD file:e8d512b08fe2ddc6f2c85831c73e4c72b9c850fa428913d19da4bb1a34f84cf2 in / 
# Tue, 29 Mar 2022 00:22:08 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:29:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:29:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 29 Mar 2022 17:30:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 22:08:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 22:08:57 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:19:34 GMT
ENV GOLANG_VERSION=1.18.1
# Wed, 13 Apr 2022 02:19:47 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18.1.linux-amd64.tar.gz'; 			sha256='b3b815f47ababac13810fc6021eb73d65478e0b2db4b09d348eefad9581a2334'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18.1.linux-armv6l.tar.gz'; 			sha256='9edc01c8e7db64e9ceeffc8258359e027812886ceca3444e83c4eb96ddb068ee'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18.1.linux-arm64.tar.gz'; 			sha256='56a91851c97fb4697077abbca38860f735c32b38993ff79b088dac46e4735633'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18.1.linux-386.tar.gz'; 			sha256='9a8df5dde9058f08ac01ecfaae42534610db398e487138788c01da26a0d41ff9'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18.1.linux-ppc64le.tar.gz'; 			sha256='33db623d1eecf362fe365107c12efc90eff0b9609e0b3345e258388019cb552a'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18.1.linux-s390x.tar.gz'; 			sha256='5d9301324148ed4dbfaa0800da43a843ffd65c834ee73fcf087255697c925f74'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 13 Apr 2022 02:19:48 GMT
ENV GOPATH=/go
# Wed, 13 Apr 2022 02:19:48 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:19:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 13 Apr 2022 02:19:49 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:dbba69284b2786013fe94fefe0c2e66a7d3cecbb20f6d691d71dac891ee37be5`  
		Last Modified: Tue, 29 Mar 2022 00:26:47 GMT  
		Size: 54.9 MB (54937710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9baf437a1badb6aad2dae5f2cd4a7b53a6c7ab6c14cba1ed1ecb42b4822b0e87`  
		Last Modified: Tue, 29 Mar 2022 17:38:08 GMT  
		Size: 5.2 MB (5155705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ade5c59e324bd7cf369c72ad781c23d37e8fb48c9bbb4abbecafafd9be4cc35`  
		Last Modified: Tue, 29 Mar 2022 17:38:08 GMT  
		Size: 10.9 MB (10874957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19a994f6d4cdbb620339bd2e4ad47b229f14276b542060622ae447649294e5d`  
		Last Modified: Tue, 29 Mar 2022 17:38:33 GMT  
		Size: 54.6 MB (54576420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c59fd148bed37342299df52e64edd44cacda6c49e334a8de0da234d5e6beb5`  
		Last Modified: Wed, 30 Mar 2022 22:12:11 GMT  
		Size: 85.8 MB (85835395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe55ee977f1346e3b36b3843bac1a122aeafcf917bc14c380b7f8612650124a`  
		Last Modified: Wed, 13 Apr 2022 02:28:57 GMT  
		Size: 141.7 MB (141701141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c5fd124f19893ecdcc4f0533a3ef8e3411a80aef3e90d608e3488ba5c18d36`  
		Last Modified: Wed, 13 Apr 2022 02:28:38 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - linux; arm variant v5

```console
$ docker pull golang@sha256:1d7e627c26ac2803cc82358e59878d2d1da21485384d0ffd924e2eadca335960
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.7 MB (301663358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:504069d8fe72929b065fbc64a67aee7a0212e375b6a955ab8c4e8adc3b78aa0d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:50:03 GMT
ADD file:6cca5eca42975074f53a45a9b4ba83d1f06b95182dd4d8d95622d63cbc206574 in / 
# Tue, 29 Mar 2022 00:50:04 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 07:42:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 07:43:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 29 Mar 2022 07:43:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 15:09:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 15:09:15 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:48:31 GMT
ENV GOLANG_VERSION=1.18.1
# Wed, 13 Apr 2022 02:53:07 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18.1.linux-amd64.tar.gz'; 			sha256='b3b815f47ababac13810fc6021eb73d65478e0b2db4b09d348eefad9581a2334'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18.1.linux-armv6l.tar.gz'; 			sha256='9edc01c8e7db64e9ceeffc8258359e027812886ceca3444e83c4eb96ddb068ee'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18.1.linux-arm64.tar.gz'; 			sha256='56a91851c97fb4697077abbca38860f735c32b38993ff79b088dac46e4735633'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18.1.linux-386.tar.gz'; 			sha256='9a8df5dde9058f08ac01ecfaae42534610db398e487138788c01da26a0d41ff9'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18.1.linux-ppc64le.tar.gz'; 			sha256='33db623d1eecf362fe365107c12efc90eff0b9609e0b3345e258388019cb552a'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18.1.linux-s390x.tar.gz'; 			sha256='5d9301324148ed4dbfaa0800da43a843ffd65c834ee73fcf087255697c925f74'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 13 Apr 2022 02:53:08 GMT
ENV GOPATH=/go
# Wed, 13 Apr 2022 02:53:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:53:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 13 Apr 2022 02:53:11 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cfb93eae062e68427eb7e96f51a690313db08e4118ca20b5a644c29fecb784db`  
		Last Modified: Tue, 29 Mar 2022 01:04:42 GMT  
		Size: 52.5 MB (52475868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d69db2a0aac9ea7e48801a42d0b5e9e3a116bd0cdc20079aea745dd5653a7a`  
		Last Modified: Tue, 29 Mar 2022 08:05:43 GMT  
		Size: 5.1 MB (5065379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcddb47fa9924cdf33c6afa828fb4fa1365d464069ed1a63a5063b7daabbabe1`  
		Last Modified: Tue, 29 Mar 2022 08:05:45 GMT  
		Size: 10.6 MB (10572944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a5b09c9df3962b241df6ed71a37e9f3febeec33fcff083e6417ada9551f79c`  
		Last Modified: Tue, 29 Mar 2022 08:06:39 GMT  
		Size: 52.3 MB (52316733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d448eaf3e3a3b08e5c04bef6900e3783b50ad674b4d05c81e0987016512b3754`  
		Last Modified: Wed, 30 Mar 2022 15:29:08 GMT  
		Size: 68.8 MB (68766145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f7125635f0a0acefa08f2b3bdc25bee4c4a4cf84c39993d2976749e0758d97`  
		Last Modified: Wed, 13 Apr 2022 03:08:40 GMT  
		Size: 112.5 MB (112466133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9b50ea7305bd094875e1df3e4dfa9fd3ae0585688640d70242d3f209a57ac6`  
		Last Modified: Wed, 13 Apr 2022 03:07:25 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - linux; arm variant v7

```console
$ docker pull golang@sha256:92f6794c9968bf14c0aadd6032c0c43ab64e485ec6069b40a9b94dfa31645e9b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.4 MB (290410849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73871b0bb7a0f2abe029dc072c99d5dbde322bf1d9ce8b2428fe029ac93f4d34`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 02:17:58 GMT
ADD file:d8d3280d101d611090968c237af923598174e090c533c24bcee805d174e4a6f5 in / 
# Tue, 29 Mar 2022 02:17:59 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 20:06:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 20:06:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 20:07:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 31 Mar 2022 23:29:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 31 Mar 2022 23:29:13 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 04:14:09 GMT
ENV GOLANG_VERSION=1.18.1
# Wed, 13 Apr 2022 04:14:43 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18.1.linux-amd64.tar.gz'; 			sha256='b3b815f47ababac13810fc6021eb73d65478e0b2db4b09d348eefad9581a2334'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18.1.linux-armv6l.tar.gz'; 			sha256='9edc01c8e7db64e9ceeffc8258359e027812886ceca3444e83c4eb96ddb068ee'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18.1.linux-arm64.tar.gz'; 			sha256='56a91851c97fb4697077abbca38860f735c32b38993ff79b088dac46e4735633'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18.1.linux-386.tar.gz'; 			sha256='9a8df5dde9058f08ac01ecfaae42534610db398e487138788c01da26a0d41ff9'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18.1.linux-ppc64le.tar.gz'; 			sha256='33db623d1eecf362fe365107c12efc90eff0b9609e0b3345e258388019cb552a'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18.1.linux-s390x.tar.gz'; 			sha256='5d9301324148ed4dbfaa0800da43a843ffd65c834ee73fcf087255697c925f74'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 13 Apr 2022 04:14:45 GMT
ENV GOPATH=/go
# Wed, 13 Apr 2022 04:14:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 04:14:47 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 13 Apr 2022 04:14:48 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fc87a15f2d540adb88546a549e56aa0a378d5719bbfd07399e467a095e27d5df`  
		Last Modified: Tue, 29 Mar 2022 02:33:28 GMT  
		Size: 50.1 MB (50133868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7991e015792e592929b68328873d303aff48f6941208e2954283895889e665b3`  
		Last Modified: Wed, 30 Mar 2022 20:30:28 GMT  
		Size: 4.9 MB (4924893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4aa6896142430c96d4b31e28c4d0e3c383d9ae671ce052f26fc7cf68189c058`  
		Last Modified: Wed, 30 Mar 2022 20:30:30 GMT  
		Size: 10.2 MB (10217881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e907cedb6582c6203cece538aac031ac66936e9249b00577dfd745a466ff936c`  
		Last Modified: Wed, 30 Mar 2022 21:30:51 GMT  
		Size: 50.3 MB (50328564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40dbe001d369848fb66eaefb3e91b9b90a56d0255de1aa23eeb28f9be23e195b`  
		Last Modified: Thu, 31 Mar 2022 23:39:20 GMT  
		Size: 64.8 MB (64787857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4b16d41f059fb5c011d6e9ee0ea05595608f70b5cf5d2db26f567c11d8431f`  
		Last Modified: Wed, 13 Apr 2022 04:38:01 GMT  
		Size: 110.0 MB (110017630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a51b6e66f2e8870c24e1afaffcdedccc386f3d03905a5357314028b12ad3c1e1`  
		Last Modified: Wed, 13 Apr 2022 04:36:47 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:301d39546808488f001760626a904b6aa4bb6e8f94a79bdd43776d990ad6c28e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.6 MB (313649299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14db0b081523f8dd4742a0f0a9df9519941a513387b6e9402c257f565fbbe94b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:01 GMT
ADD file:5e8f8c10da6d37a727fb5e1ed13b3dd78769f0ca7e91f0c3510e2edd25177117 in / 
# Tue, 29 Mar 2022 00:43:03 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:13:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 02:13:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 02:13:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 22:45:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 22:45:07 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:39:52 GMT
ENV GOLANG_VERSION=1.18.1
# Wed, 13 Apr 2022 02:40:03 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18.1.linux-amd64.tar.gz'; 			sha256='b3b815f47ababac13810fc6021eb73d65478e0b2db4b09d348eefad9581a2334'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18.1.linux-armv6l.tar.gz'; 			sha256='9edc01c8e7db64e9ceeffc8258359e027812886ceca3444e83c4eb96ddb068ee'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18.1.linux-arm64.tar.gz'; 			sha256='56a91851c97fb4697077abbca38860f735c32b38993ff79b088dac46e4735633'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18.1.linux-386.tar.gz'; 			sha256='9a8df5dde9058f08ac01ecfaae42534610db398e487138788c01da26a0d41ff9'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18.1.linux-ppc64le.tar.gz'; 			sha256='33db623d1eecf362fe365107c12efc90eff0b9609e0b3345e258388019cb552a'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18.1.linux-s390x.tar.gz'; 			sha256='5d9301324148ed4dbfaa0800da43a843ffd65c834ee73fcf087255697c925f74'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 13 Apr 2022 02:40:05 GMT
ENV GOPATH=/go
# Wed, 13 Apr 2022 02:40:06 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:40:07 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 13 Apr 2022 02:40:08 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fa223d8c149d7beec8e997e1415ee4961473cafaf88a932f70baf3da56f2c564`  
		Last Modified: Tue, 29 Mar 2022 00:49:33 GMT  
		Size: 53.6 MB (53633710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ffbd2ab15985c19f9e1e3199cdce06090266d20d11dbd3d55fba45de2fcc27`  
		Last Modified: Wed, 30 Mar 2022 02:24:13 GMT  
		Size: 4.9 MB (4938638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3953e76cee2ab175d909ccec1a3399912a690ad621ae88cff787d98419b97bb`  
		Last Modified: Wed, 30 Mar 2022 02:24:14 GMT  
		Size: 10.7 MB (10656993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f906570592fdd65a2fcfae6164990d0422e03ccadba25c5b1d1268a29f7c530`  
		Last Modified: Wed, 30 Mar 2022 02:24:36 GMT  
		Size: 54.7 MB (54671703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab4554a324ffb6819185363bc0c712884b762f5ef35c6b730401e1ef6a6be44b`  
		Last Modified: Wed, 30 Mar 2022 22:49:39 GMT  
		Size: 81.0 MB (81049834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6a3531de7f6c589885b2497c7066c217cab01a92ad98f31220f70d7768a9a0`  
		Last Modified: Wed, 13 Apr 2022 02:49:57 GMT  
		Size: 108.7 MB (108698295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9123ccc7632a6015d2134eb7f44eb5d078e6d45304b5e4106539ee9363a7feb`  
		Last Modified: Wed, 13 Apr 2022 02:49:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - linux; 386

```console
$ docker pull golang@sha256:37574560ebbd539761a9520788621076ab067ae3208c9fa0093e79baf599f49f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.9 MB (327884045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9bfb9c4b5fd1f9158c7be0bec7ffd118f8d8f34da46e36cbaab242e316a4350`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:41:45 GMT
ADD file:378357c2fb82d0ee5366dc2926393bb2779a44632ebb0b9cb95919df6d60fcc5 in / 
# Tue, 29 Mar 2022 00:41:46 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:56:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:56:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 29 Mar 2022 17:56:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 00:53:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 00:53:09 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:38:34 GMT
ENV GOLANG_VERSION=1.18.1
# Wed, 13 Apr 2022 02:38:49 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18.1.linux-amd64.tar.gz'; 			sha256='b3b815f47ababac13810fc6021eb73d65478e0b2db4b09d348eefad9581a2334'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18.1.linux-armv6l.tar.gz'; 			sha256='9edc01c8e7db64e9ceeffc8258359e027812886ceca3444e83c4eb96ddb068ee'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18.1.linux-arm64.tar.gz'; 			sha256='56a91851c97fb4697077abbca38860f735c32b38993ff79b088dac46e4735633'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18.1.linux-386.tar.gz'; 			sha256='9a8df5dde9058f08ac01ecfaae42534610db398e487138788c01da26a0d41ff9'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18.1.linux-ppc64le.tar.gz'; 			sha256='33db623d1eecf362fe365107c12efc90eff0b9609e0b3345e258388019cb552a'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18.1.linux-s390x.tar.gz'; 			sha256='5d9301324148ed4dbfaa0800da43a843ffd65c834ee73fcf087255697c925f74'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 13 Apr 2022 02:38:50 GMT
ENV GOPATH=/go
# Wed, 13 Apr 2022 02:38:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:38:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 13 Apr 2022 02:38:53 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:861044c168563defddcd8a95bf60383713febc9f81711ebacce77cb8d8bb6025`  
		Last Modified: Tue, 29 Mar 2022 00:48:28 GMT  
		Size: 55.9 MB (55940697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d406d9f02e821bb3474a359f0c2ac4aeedd79b542f20f04bcc186e4736110e60`  
		Last Modified: Tue, 29 Mar 2022 18:14:55 GMT  
		Size: 5.1 MB (5080188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c749cbf8729279672e08b490f3e525398234a747f98239ef023cb89024834da`  
		Last Modified: Tue, 29 Mar 2022 18:14:56 GMT  
		Size: 11.0 MB (11033883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a0bf6dbfc9ef788600d23b4a23105529cb3e544a7ec60f2c4874ddea1226f90`  
		Last Modified: Tue, 29 Mar 2022 18:15:21 GMT  
		Size: 55.9 MB (55913455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0a0e8cea367ee486f1e6e28cd181756f1edc1116be0c68afb72f64df1bcd44`  
		Last Modified: Wed, 30 Mar 2022 00:58:21 GMT  
		Size: 87.1 MB (87059857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a51d5965cedad9572927268cfe195b9e0123a68ffa4167b2233f24365f7be631`  
		Last Modified: Wed, 13 Apr 2022 02:50:10 GMT  
		Size: 112.9 MB (112855838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b326f760d344ff7cd3c5ca9e719caaf1fb28635b1c6770dde1eced45e546b107`  
		Last Modified: Wed, 13 Apr 2022 02:49:56 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - linux; mips64le

```console
$ docker pull golang@sha256:e139e689507eb71b946b5bd7ac89e9b42635163b4fc0454361d910d62adf04cf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.5 MB (297467552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aa49472658c3e1463040ec08cb54ce1f850459eca04deee5f8ef95a06de82aa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 07:41:51 GMT
ADD file:40fc6f06ccce55e9889d1c94556c29242d1ac62870cb9895da64d37bac45ab5e in / 
# Tue, 29 Mar 2022 07:41:56 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 08:27:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 08:27:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 29 Mar 2022 08:29:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 31 Mar 2022 01:47:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 31 Mar 2022 01:47:25 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:07:26 GMT
ENV GOLANG_VERSION=1.18.1
# Wed, 13 Apr 2022 02:19:09 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18.1.linux-amd64.tar.gz'; 			sha256='b3b815f47ababac13810fc6021eb73d65478e0b2db4b09d348eefad9581a2334'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18.1.linux-armv6l.tar.gz'; 			sha256='9edc01c8e7db64e9ceeffc8258359e027812886ceca3444e83c4eb96ddb068ee'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18.1.linux-arm64.tar.gz'; 			sha256='56a91851c97fb4697077abbca38860f735c32b38993ff79b088dac46e4735633'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18.1.linux-386.tar.gz'; 			sha256='9a8df5dde9058f08ac01ecfaae42534610db398e487138788c01da26a0d41ff9'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18.1.linux-ppc64le.tar.gz'; 			sha256='33db623d1eecf362fe365107c12efc90eff0b9609e0b3345e258388019cb552a'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18.1.linux-s390x.tar.gz'; 			sha256='5d9301324148ed4dbfaa0800da43a843ffd65c834ee73fcf087255697c925f74'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 13 Apr 2022 02:19:17 GMT
ENV GOPATH=/go
# Wed, 13 Apr 2022 02:19:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:19:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 13 Apr 2022 02:19:40 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:efb90a274e1b19eec263e44f7fbc1f9c9c6c393210c27b03ebde7c2b0a2b6482`  
		Last Modified: Tue, 29 Mar 2022 07:52:16 GMT  
		Size: 53.2 MB (53199386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7959b932ae1363e586ef79fc1ab6afdaee0b7a9f97e0a507c1868cfc6dd47778`  
		Last Modified: Tue, 29 Mar 2022 08:57:32 GMT  
		Size: 4.9 MB (4912295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3b22f54d8b49fd2d7d246274c6016cdcff9377c15befaa4323d44c3b1e75ac`  
		Last Modified: Tue, 29 Mar 2022 08:57:35 GMT  
		Size: 10.7 MB (10660105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d388c5955683d48c342f8d6b2291b7cedf59d2fcfb9343f5aa240f4b5f56da3`  
		Last Modified: Tue, 29 Mar 2022 08:58:23 GMT  
		Size: 53.3 MB (53297457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e978f1552505ee0749721ea9d15cea9c7bdcfec2486a888d0f42104c476513`  
		Last Modified: Thu, 31 Mar 2022 02:37:01 GMT  
		Size: 66.7 MB (66736753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2264854fd070c3191d53e3ebb7e1a728cb5c563d4d825c1d4aadc28228169aa8`  
		Last Modified: Wed, 13 Apr 2022 02:56:18 GMT  
		Size: 108.7 MB (108661430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79083f084a68eb86a8f8650ebad60bd217b164c06376c32e645cda52840f6347`  
		Last Modified: Wed, 13 Apr 2022 02:55:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - linux; ppc64le

```console
$ docker pull golang@sha256:3d833a08e829e4a9da7873b2391d839ff29db6c59462a145b171a04da2adfc32
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.9 MB (323918426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f86f74db99f2ccbb4a6b5060d10ba429f1d3f680fab58c3a2b192ae28a4226c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:21:35 GMT
ADD file:32dd723ee02b792cb3de67b78d352e79bdb52bf9d23fa5190ce764956b1e3884 in / 
# Tue, 29 Mar 2022 00:21:42 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 05:47:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 05:48:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 05:50:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 31 Mar 2022 13:31:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 31 Mar 2022 13:31:28 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:40:30 GMT
ENV GOLANG_VERSION=1.18.1
# Wed, 13 Apr 2022 02:41:07 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18.1.linux-amd64.tar.gz'; 			sha256='b3b815f47ababac13810fc6021eb73d65478e0b2db4b09d348eefad9581a2334'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18.1.linux-armv6l.tar.gz'; 			sha256='9edc01c8e7db64e9ceeffc8258359e027812886ceca3444e83c4eb96ddb068ee'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18.1.linux-arm64.tar.gz'; 			sha256='56a91851c97fb4697077abbca38860f735c32b38993ff79b088dac46e4735633'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18.1.linux-386.tar.gz'; 			sha256='9a8df5dde9058f08ac01ecfaae42534610db398e487138788c01da26a0d41ff9'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18.1.linux-ppc64le.tar.gz'; 			sha256='33db623d1eecf362fe365107c12efc90eff0b9609e0b3345e258388019cb552a'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18.1.linux-s390x.tar.gz'; 			sha256='5d9301324148ed4dbfaa0800da43a843ffd65c834ee73fcf087255697c925f74'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 13 Apr 2022 02:41:14 GMT
ENV GOPATH=/go
# Wed, 13 Apr 2022 02:41:17 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:41:25 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 13 Apr 2022 02:41:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c632eeaf13829ddb578e0545ba882dab1aee70ee0cf3069a1fc9eefd23c3e0a8`  
		Last Modified: Tue, 29 Mar 2022 00:32:02 GMT  
		Size: 58.8 MB (58834937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:762034bf4e697addca3a77a00590017f45c852584700ffabe39eed10a6c58083`  
		Last Modified: Wed, 30 Mar 2022 06:25:30 GMT  
		Size: 5.4 MB (5405164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c92df217f6ce5e8db50ab0c999242f4d0fbefce03ed9a33195642d3c86ce17`  
		Last Modified: Wed, 30 Mar 2022 06:25:31 GMT  
		Size: 11.6 MB (11627455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543ec63f3430a7907602f65d568921eac8baffc304cc47afd544b1d44996285f`  
		Last Modified: Wed, 30 Mar 2022 06:25:58 GMT  
		Size: 58.9 MB (58854169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7ba7ad317c2e615ec8a60451c28111c6feef1be0090a403822e3dbd1b716c9`  
		Last Modified: Thu, 31 Mar 2022 13:42:53 GMT  
		Size: 80.3 MB (80318194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db9efeaba138a2395c86950e9e17a81d49fc905aba84bae02230603b5e88afe`  
		Last Modified: Wed, 13 Apr 2022 02:56:25 GMT  
		Size: 108.9 MB (108878351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2db06209de29e0cf000a9f486159a2d53757d8afe812f894beb6e19152b24c7`  
		Last Modified: Wed, 13 Apr 2022 02:55:55 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - linux; s390x

```console
$ docker pull golang@sha256:f60f21ce4c5ccab9f33873cc648b7419f423e7649bf48df896d69988f709d5b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.3 MB (300331510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4904070d6abbe0b74af32ad5b27583f456d60ba74c894c4df9af846d5de05029`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:51:38 GMT
ADD file:3239542512469e874d06b7deba00e80df79d7544038304df05ee6484a85757be in / 
# Tue, 29 Mar 2022 00:51:40 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:25:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 02:25:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 02:25:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 19:37:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 19:37:32 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:41:34 GMT
ENV GOLANG_VERSION=1.18.1
# Wed, 13 Apr 2022 02:41:55 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18.1.linux-amd64.tar.gz'; 			sha256='b3b815f47ababac13810fc6021eb73d65478e0b2db4b09d348eefad9581a2334'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18.1.linux-armv6l.tar.gz'; 			sha256='9edc01c8e7db64e9ceeffc8258359e027812886ceca3444e83c4eb96ddb068ee'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18.1.linux-arm64.tar.gz'; 			sha256='56a91851c97fb4697077abbca38860f735c32b38993ff79b088dac46e4735633'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18.1.linux-386.tar.gz'; 			sha256='9a8df5dde9058f08ac01ecfaae42534610db398e487138788c01da26a0d41ff9'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18.1.linux-ppc64le.tar.gz'; 			sha256='33db623d1eecf362fe365107c12efc90eff0b9609e0b3345e258388019cb552a'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18.1.linux-s390x.tar.gz'; 			sha256='5d9301324148ed4dbfaa0800da43a843ffd65c834ee73fcf087255697c925f74'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18.1.src.tar.gz'; 		sha256='efd43e0f1402e083b73a03d444b7b6576bb4c539ac46208b63a916b69aca4088'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 13 Apr 2022 02:42:03 GMT
ENV GOPATH=/go
# Wed, 13 Apr 2022 02:42:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Apr 2022 02:42:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 13 Apr 2022 02:42:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c9bfa2e596807d7800fe5f547e2f9a23f962c4657b2a6f9d9060de9104720bbe`  
		Last Modified: Tue, 29 Mar 2022 01:00:56 GMT  
		Size: 53.2 MB (53210113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0aa1eaca1c86da823fdc122ec5b9164785c313246353b48d09df732b7a8c99`  
		Last Modified: Wed, 30 Mar 2022 02:33:40 GMT  
		Size: 5.1 MB (5140495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7602591a16786e579b57880b05147a0e9565af67feba9ac9610d29ecb8ff3d78`  
		Last Modified: Wed, 30 Mar 2022 02:33:40 GMT  
		Size: 10.8 MB (10765166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb97d88322672ae9d245cbe2062fdc59dd157f2d26ea4c65605b14c6dd8253bf`  
		Last Modified: Wed, 30 Mar 2022 02:33:56 GMT  
		Size: 54.0 MB (54044630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0852a014377011daa14f33105fce183a1a8624b36176f3f7c98ead85554fdca3`  
		Last Modified: Wed, 30 Mar 2022 19:41:23 GMT  
		Size: 65.6 MB (65560744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:558e87105df48e948670ff761a95768cbcc76825eacc1b4f4de03160eba86bab`  
		Last Modified: Wed, 13 Apr 2022 02:53:43 GMT  
		Size: 111.6 MB (111610206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e40921d1c5bcf23b831c2c322c77d27d4decff89996038113330f838989d66a3`  
		Last Modified: Wed, 13 Apr 2022 02:53:28 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - windows version 10.0.20348.643; amd64

```console
$ docker pull golang@sha256:d267da70653d05c87abe1e698a645a469796a190e19d9a88cefa208136aae4b4
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2406120590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8632a3f0ec672f88e20a6058d3d32d448e91dc2de1b25b7b75fbc76ca797009`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 03 Apr 2022 05:50:25 GMT
RUN Install update ltsc2022-amd64
# Wed, 13 Apr 2022 02:27:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 02:27:59 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 Apr 2022 02:28:00 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 Apr 2022 02:28:01 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 Apr 2022 02:28:02 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 Apr 2022 02:29:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Apr 2022 02:29:19 GMT
ENV GOPATH=C:\go
# Wed, 13 Apr 2022 02:30:07 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Apr 2022 02:30:08 GMT
ENV GOLANG_VERSION=1.18.1
# Wed, 13 Apr 2022 02:33:47 GMT
RUN $url = 'https://dl.google.com/go/go1.18.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'c30bc3f1f7314a953fe208bd9cd5e24bd9403392a6c556ced3677f9f70f71fe1'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Apr 2022 02:33:49 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dccd9e4d14d3d5a6e93f87350b903e117368ada32d711986f779b5a3ef8657cc`  
		Size: 975.3 MB (975255801 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1ab01d498c34190a1e49e15239442a41312c6ea5904e18f186f84f90f11fc422`  
		Last Modified: Wed, 13 Apr 2022 03:13:51 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46df2c1d7d7b9748c6ddb8e9f196dfb2526451470a1256ab4047bece8468ff7a`  
		Last Modified: Wed, 13 Apr 2022 03:13:50 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9395e3155b04f913275d2f0e2bd07626c8d9b889b0646bb3fb44414d2df4130d`  
		Last Modified: Wed, 13 Apr 2022 03:13:44 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3d0b098f175d5015767a5bb9a5641f1a1966ea2e2863b55cae5ae54f7edeb9`  
		Last Modified: Wed, 13 Apr 2022 03:13:44 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff921731e5c58ad62f0eb62e698dd3033694fd15898c3e94d8021c0097dd912`  
		Last Modified: Wed, 13 Apr 2022 03:13:44 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19b89723742f5296cfb0b6d93c8b65a4995ee4a964d59eae8e96557dffc8f9e`  
		Last Modified: Wed, 13 Apr 2022 03:14:02 GMT  
		Size: 25.7 MB (25714775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ab0e7bcbbef7fb8a566a25556fc4b487c323359badbd7ab1bc58ab41729a7a`  
		Last Modified: Wed, 13 Apr 2022 03:13:40 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f67794576dcaaf4ef811c935b4ed0b40efe1487f0d0ab09462473b606d1fd89`  
		Last Modified: Wed, 13 Apr 2022 03:13:40 GMT  
		Size: 562.2 KB (562186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2932986f0f385a406d2115ccb58dbf32a1730cf7e1f7f9f520863fcaa3e20d64`  
		Last Modified: Wed, 13 Apr 2022 03:13:40 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f896ebd03d7af93409bcfb6bbbbd64481e6f575754cf0c600003a48a32d7a0b`  
		Last Modified: Wed, 13 Apr 2022 03:14:42 GMT  
		Size: 152.9 MB (152877366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f82b1974e8addd899731575590ff20cf09b3e97cdfe2ed285fc081b742b331`  
		Last Modified: Wed, 13 Apr 2022 03:13:40 GMT  
		Size: 1.6 KB (1551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - windows version 10.0.17763.2803; amd64

```console
$ docker pull golang@sha256:9310002d25ff89a01e1e11afefd6a2455e45f69022f3fd2eea74d2270286c511
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2894358142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ade0022898cad2ad609f053cba2f938006a5ecf4e638ef7f61298f032c9fa02`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 04 Apr 2022 11:20:25 GMT
RUN Install update 1809-amd64
# Wed, 13 Apr 2022 02:34:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Apr 2022 02:34:09 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 Apr 2022 02:34:10 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 Apr 2022 02:34:13 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 Apr 2022 02:34:22 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 Apr 2022 02:37:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Apr 2022 02:37:05 GMT
ENV GOPATH=C:\go
# Wed, 13 Apr 2022 02:38:54 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Apr 2022 02:38:55 GMT
ENV GOLANG_VERSION=1.18.1
# Wed, 13 Apr 2022 02:43:27 GMT
RUN $url = 'https://dl.google.com/go/go1.18.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'c30bc3f1f7314a953fe208bd9cd5e24bd9403392a6c556ced3677f9f70f71fe1'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Apr 2022 02:43:29 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba8181afd4264392fbbf8df14fb4cddc55fbe085ab000e986b789678bc2bb171`  
		Size: 997.6 MB (997587446 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba1c113303b8371787710ec139807b93d58a8b0789523fc35afdb65f6e94bc61`  
		Last Modified: Wed, 13 Apr 2022 03:15:12 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9b761254212cd472f566f902a9830a91c33e94d06fb02a0192e29fe447bf98`  
		Last Modified: Wed, 13 Apr 2022 03:15:11 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0210c142bbabba5cac6b3d06dc265578eafda02e9f54b2b955129652065abba5`  
		Last Modified: Wed, 13 Apr 2022 03:15:05 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24b5fea0cadfc385f0501b3cd52647d69ba5dd030f05bc637848ed7298ed45e`  
		Last Modified: Wed, 13 Apr 2022 03:15:04 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1490fa326c6ac4254cc7e87bd773641c1a74d6d68ef0ee562e1296aa6e5ba09`  
		Last Modified: Wed, 13 Apr 2022 03:15:04 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb5425f63a29b9eb9b5bbbf135d080f8b1d2415a665b41591175a49f41da70d`  
		Last Modified: Wed, 13 Apr 2022 03:15:23 GMT  
		Size: 25.5 MB (25453409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf5f939642f2aaa6426ec58683c461b2fc27f9b92ed53ceea3d53e5f5b8d18d`  
		Last Modified: Wed, 13 Apr 2022 03:15:01 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1523ec6181c5a38a1257f1181b0b390b0fa168627daeb103a617f04cf11c9666`  
		Last Modified: Wed, 13 Apr 2022 03:15:01 GMT  
		Size: 328.4 KB (328368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79bd1c12294b889070c52d26bdf131e7ce486995b882ef03a636067463c32399`  
		Last Modified: Wed, 13 Apr 2022 03:15:00 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9acc730fd2b8555b101c85bba2a49a122e8815d9810165140a08c0b4c1ddc1`  
		Last Modified: Wed, 13 Apr 2022 03:16:04 GMT  
		Size: 152.6 MB (152644506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d24b1933c37e869723390f1e950e9579cb32d121540a2b0fc137c3b1a87e7d`  
		Last Modified: Wed, 13 Apr 2022 03:15:00 GMT  
		Size: 1.5 KB (1541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
