## `golang:1-buster`

```console
$ docker pull golang@sha256:c0a5d0971eea7fd1696393cda38ee32667cc97aa4246a722a369f106de9ab069
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

### `golang:1-buster` - linux; amd64

```console
$ docker pull golang@sha256:b6fe2cc154c1be5fe9dbd7cf5f23f5f48126946762d5ab547ed9a5d2f7562fa3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.6 MB (323647188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d23d83b05a3284f31a481d309f5a4878a19bd5a42672914ea5d3e287dfc574`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:30 GMT
ADD file:e952f6979e4b0ead00b6906db1dd70eb9beb564a04e2f02e2e0cff8614920216 in / 
# Thu, 22 Jul 2021 00:45:31 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 01:12:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:12:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 01:12:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 02:01:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 02:01:18 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Aug 2021 01:35:54 GMT
ENV GOLANG_VERSION=1.17
# Tue, 17 Aug 2021 01:36:06 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.17.linux-amd64.tar.gz'; 			sha256='6bf89fc4f5ad763871cf7eac80a2d594492de7a818303283f1366a7f6a30372d'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.linux-armv6l.tar.gz'; 			sha256='ae89d33f4e4acc222bdb04331933d5ece4ae71039812f6ccd7493cb3e8ddfb4e'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.linux-arm64.tar.gz'; 			sha256='01a9af009ada22122d3fcb9816049c1d21842524b38ef5d5a0e2ee4b26d7c3e7'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.linux-386.tar.gz'; 			sha256='c19e3227a6ac6329db91d1af77bbf239ccd760a259c16e6b9c932d527ff14848'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.linux-ppc64le.tar.gz'; 			sha256='ee84350114d532bf15f096198c675aafae9ff091dc4cc69eb49e1817ff94dbd7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.linux-s390x.tar.gz'; 			sha256='a50aaecf054f393575f969a9105d5c6864dd91afc5287d772449033fbafcf7e3'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.src.tar.gz'; 		sha256='3a70e5055509f347c0fb831ca07a2bf3b531068f349b14a3c652e9b5b67beb5d'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Tue, 17 Aug 2021 01:36:07 GMT
ENV GOPATH=/go
# Tue, 17 Aug 2021 01:36:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Aug 2021 01:36:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 17 Aug 2021 01:36:09 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:627b765e08d177e63c9a202ca4991b711448905b934435c70b7cbd7d4a9c7959`  
		Last Modified: Thu, 22 Jul 2021 00:50:07 GMT  
		Size: 50.4 MB (50435626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c040670e5e559fd936db175530ad4c1dd014bd25b2bf25ea19fa20554fe2d736`  
		Last Modified: Thu, 22 Jul 2021 01:19:54 GMT  
		Size: 7.8 MB (7832944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073a180f4992853fa3dd8da604e7b041bc8ea92157749d042c0853312f178f6a`  
		Last Modified: Thu, 22 Jul 2021 01:19:54 GMT  
		Size: 10.0 MB (9997222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf76209566d0c8d78df205b09e6e5b52ff7f10cb4e1c03d9336ed7dd2decd919`  
		Last Modified: Thu, 22 Jul 2021 01:20:16 GMT  
		Size: 51.8 MB (51841203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6182a456504bb119011b721ede5d1e6cf4d0621447465d80cc1d4e53c0ef95e6`  
		Last Modified: Fri, 23 Jul 2021 02:05:30 GMT  
		Size: 68.7 MB (68749967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f43dfc05459a183e0c40885f545b8fc7bf2af4eb5ae1ca35526e9217d19f08e`  
		Last Modified: Tue, 17 Aug 2021 01:43:40 GMT  
		Size: 134.8 MB (134790071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8b069154e6fe74fcadb2527496424a9ffb6902faaa6b8c40a69f275cc9e5112`  
		Last Modified: Tue, 17 Aug 2021 01:43:20 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; arm variant v5

```console
$ docker pull golang@sha256:6f662572d1418bd32d87ff8f6fe0e87aa4bbff74b6468f6d90d8df0202c9034c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269381401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690e15c67a83da6740715f1ab841325a95e77ff575abfc79168f7ccb2f172f39`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:49:34 GMT
ADD file:4a4158b5432e31cd686b7b2874c22d86a381ac71c3146fe6746501db3d216b41 in / 
# Thu, 22 Jul 2021 00:49:35 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 02:03:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 02:03:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 02:04:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 16:11:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 16:11:20 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Aug 2021 21:48:50 GMT
ENV GOLANG_VERSION=1.16.7
# Thu, 05 Aug 2021 21:51:56 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.16.7.linux-amd64.tar.gz'; 			sha256='7fe7a73f55ba3e2285da36f8b085e5c0159e9564ef5f63ee0ed6b818ade8ef04'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.16.7.linux-armv6l.tar.gz'; 			sha256='b2973ceeae234866368baf9469fb7b9444857e50dc785ba879d98a0aa208a12b'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.16.7.linux-arm64.tar.gz'; 			sha256='63d6b53ecbd2b05c1f0e9903c92042663f2f68afdbb67f4d0d12700156869bac'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.16.7.linux-386.tar.gz'; 			sha256='5c0c8891fa88993f2193fbc9dd5cca6c250c89aa8c12bbaa382b6ff38139bcc3'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.16.7.linux-ppc64le.tar.gz'; 			sha256='03e02b2ac6dc1601203f335385b9bbe15a55677066d9a1a1280b5fcfa6ec4738'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.16.7.linux-s390x.tar.gz'; 			sha256='5f691c9551710ebb17bbda04389944aa7332f42ab28f92516a69fbd7860e7e9f'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 		sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 05 Aug 2021 21:51:58 GMT
ENV GOPATH=/go
# Thu, 05 Aug 2021 21:51:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Aug 2021 21:52:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 05 Aug 2021 21:52:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cd9bc325fb9e2673d4a4f97499e5ac67f82d24eef19ed2cb8d13af9c9256d20c`  
		Last Modified: Thu, 22 Jul 2021 01:01:22 GMT  
		Size: 48.2 MB (48153246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6ac5ad14f3066e98bd031f59bcd25af51c46975f1f67aa9e984aae49997f855`  
		Last Modified: Thu, 22 Jul 2021 02:21:02 GMT  
		Size: 7.4 MB (7376533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3538b6814e6bbc64643ef42ffb80c592cecc6833f8c77baa213b7d572de2f060`  
		Last Modified: Thu, 22 Jul 2021 02:21:02 GMT  
		Size: 9.7 MB (9687577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e98fc7d7506f4cd2a0d1ab64ad0e0a5e9863175a5bcadf61c19a25091d861d34`  
		Last Modified: Thu, 22 Jul 2021 02:21:56 GMT  
		Size: 49.6 MB (49575389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0603fa664f95d8074de109c383370a08008de46caf8d285bdc49edb42461b128`  
		Last Modified: Thu, 22 Jul 2021 16:23:47 GMT  
		Size: 52.1 MB (52056868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76d1ad1fac12546fc38c62ccb793a2619fd65db14d17e2628137f47c13c0d8a`  
		Last Modified: Thu, 05 Aug 2021 21:58:10 GMT  
		Size: 102.5 MB (102531634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5226a63e95815f4d8733d8f3a767fc0b01f10ea97eab771e801637fe0f1783`  
		Last Modified: Thu, 05 Aug 2021 21:57:05 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; arm variant v7

```console
$ docker pull golang@sha256:e0bf5671a79a4f7766afa245f3ccdfc93a0509a1e01bfb9bfbf79742dbd171a4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263248316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c5e05b4ccb8e9745569636905f284309e242584d3ee7223437d4bbd9285d38`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 02:03:13 GMT
ADD file:c33137dc0d277fe210ea6387a8be105c625fdf777a541a6392896766df9919d4 in / 
# Thu, 22 Jul 2021 02:03:14 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 04:14:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 04:15:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 04:15:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 04:46:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 04:46:10 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Aug 2021 23:01:23 GMT
ENV GOLANG_VERSION=1.16.7
# Thu, 05 Aug 2021 23:01:53 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.16.7.linux-amd64.tar.gz'; 			sha256='7fe7a73f55ba3e2285da36f8b085e5c0159e9564ef5f63ee0ed6b818ade8ef04'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.16.7.linux-armv6l.tar.gz'; 			sha256='b2973ceeae234866368baf9469fb7b9444857e50dc785ba879d98a0aa208a12b'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.16.7.linux-arm64.tar.gz'; 			sha256='63d6b53ecbd2b05c1f0e9903c92042663f2f68afdbb67f4d0d12700156869bac'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.16.7.linux-386.tar.gz'; 			sha256='5c0c8891fa88993f2193fbc9dd5cca6c250c89aa8c12bbaa382b6ff38139bcc3'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.16.7.linux-ppc64le.tar.gz'; 			sha256='03e02b2ac6dc1601203f335385b9bbe15a55677066d9a1a1280b5fcfa6ec4738'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.16.7.linux-s390x.tar.gz'; 			sha256='5f691c9551710ebb17bbda04389944aa7332f42ab28f92516a69fbd7860e7e9f'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 		sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 05 Aug 2021 23:01:55 GMT
ENV GOPATH=/go
# Thu, 05 Aug 2021 23:01:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Aug 2021 23:01:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 05 Aug 2021 23:01:58 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ff16e408fd8b8191145782047ebc0c76176550d844743a679143d53a164bea21`  
		Last Modified: Thu, 22 Jul 2021 02:15:33 GMT  
		Size: 45.9 MB (45917250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7701a3a4dc54422c371762f5416afea6835e02e9db10fd686f73159ec84ec2f7`  
		Last Modified: Thu, 22 Jul 2021 04:35:32 GMT  
		Size: 7.1 MB (7124233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8651c1854c791264fe60acc8ab39e9b914dc3258a9aa42509f1c35ce32a880d`  
		Last Modified: Thu, 22 Jul 2021 04:35:32 GMT  
		Size: 9.3 MB (9343793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14bda9bdbd404cfcf13425f9c6273b254196ada60d6315690312688674624a7`  
		Last Modified: Thu, 22 Jul 2021 04:36:20 GMT  
		Size: 47.4 MB (47356980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554e943d351eb3a69051efb53627557f7db7ba465d51dd6cdec7b91c291f379a`  
		Last Modified: Fri, 23 Jul 2021 04:56:32 GMT  
		Size: 53.2 MB (53222447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6a15f80359b0d93972af4d261f2aea5e92f1758a2fb64827948db253de64ae`  
		Last Modified: Thu, 05 Aug 2021 23:21:09 GMT  
		Size: 100.3 MB (100283458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7df7924399bcdf7b40e3085b49802a29aa4dc227df0a806fe21d505456b2daa`  
		Last Modified: Thu, 05 Aug 2021 23:20:04 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:bb4f3a1b7c31646ddfcc6fd75860bb8b0621b0cccd27f59b62a0ec12aca77852
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.3 MB (284277436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b090f05cd83a2e2d21f5cdaf589c6f096be16db5b5a0cc9803931dbe1548fb03`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:39:59 GMT
ADD file:3e8e075f08a6b727602af05c539f43648a48663cbb3a88eeba310cfc32c01d78 in / 
# Thu, 22 Jul 2021 00:40:00 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 01:15:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:16:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 01:16:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 13:32:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 13:32:20 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Aug 2021 02:00:46 GMT
ENV GOLANG_VERSION=1.17
# Tue, 17 Aug 2021 02:00:57 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.17.linux-amd64.tar.gz'; 			sha256='6bf89fc4f5ad763871cf7eac80a2d594492de7a818303283f1366a7f6a30372d'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.linux-armv6l.tar.gz'; 			sha256='ae89d33f4e4acc222bdb04331933d5ece4ae71039812f6ccd7493cb3e8ddfb4e'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.linux-arm64.tar.gz'; 			sha256='01a9af009ada22122d3fcb9816049c1d21842524b38ef5d5a0e2ee4b26d7c3e7'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.linux-386.tar.gz'; 			sha256='c19e3227a6ac6329db91d1af77bbf239ccd760a259c16e6b9c932d527ff14848'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.linux-ppc64le.tar.gz'; 			sha256='ee84350114d532bf15f096198c675aafae9ff091dc4cc69eb49e1817ff94dbd7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.linux-s390x.tar.gz'; 			sha256='a50aaecf054f393575f969a9105d5c6864dd91afc5287d772449033fbafcf7e3'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.src.tar.gz'; 		sha256='3a70e5055509f347c0fb831ca07a2bf3b531068f349b14a3c652e9b5b67beb5d'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Tue, 17 Aug 2021 02:00:58 GMT
ENV GOPATH=/go
# Tue, 17 Aug 2021 02:00:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Aug 2021 02:00:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 17 Aug 2021 02:00:59 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d272b0d8f7c4fd0caf0ef022ce544cfe3800e349a73b585f82837e6526a4247e`  
		Last Modified: Thu, 22 Jul 2021 00:45:18 GMT  
		Size: 49.2 MB (49222109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81fabd82f026fa10e0e0341fa3d6d3112de04413ea6c46e72bcc1dca40d924aa`  
		Last Modified: Thu, 22 Jul 2021 01:25:00 GMT  
		Size: 7.7 MB (7694906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0193c0cdceae23cd0e13721651d74f409440171fe8a1c8b521616b6ed29db6e1`  
		Last Modified: Thu, 22 Jul 2021 01:25:00 GMT  
		Size: 10.0 MB (9984335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:967a8f1385966af47c9f250997e3158c319d498adc004c91570f770ceac5045a`  
		Last Modified: Thu, 22 Jul 2021 01:25:24 GMT  
		Size: 52.2 MB (52167528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f10b34911491399aa2caeb545e897b4fd44568636b77f650887a40f2e08e4e1`  
		Last Modified: Thu, 22 Jul 2021 13:36:49 GMT  
		Size: 62.6 MB (62616191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c72bc055ffc9d98ba62f7c6098d88dceb568bb55c74cb8414cf3671f5d22ee9`  
		Last Modified: Tue, 17 Aug 2021 02:08:03 GMT  
		Size: 102.6 MB (102592210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5177f872f98ad2ba08145e55f67970baffc8e9cd826b217e079f8f312d1428`  
		Last Modified: Tue, 17 Aug 2021 02:07:46 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; 386

```console
$ docker pull golang@sha256:633dff80ab7628865ee68d090ccc2fe52c7b6b9c9e34dcb7250f4efcfbc98dd0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299686951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18793c906efe28e4db92736c27b430b3b6c462e9aedd95c39f2d72402539204b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:39:33 GMT
ADD file:574afb2f0b9121fa552563f323a2edd9a3aa71fc927a280c3eb9cbbf944a12ff in / 
# Thu, 22 Jul 2021 00:39:34 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 04:05:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 04:05:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 04:05:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 17:28:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 17:28:04 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Aug 2021 21:40:09 GMT
ENV GOLANG_VERSION=1.16.7
# Thu, 05 Aug 2021 21:40:33 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.16.7.linux-amd64.tar.gz'; 			sha256='7fe7a73f55ba3e2285da36f8b085e5c0159e9564ef5f63ee0ed6b818ade8ef04'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.16.7.linux-armv6l.tar.gz'; 			sha256='b2973ceeae234866368baf9469fb7b9444857e50dc785ba879d98a0aa208a12b'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.16.7.linux-arm64.tar.gz'; 			sha256='63d6b53ecbd2b05c1f0e9903c92042663f2f68afdbb67f4d0d12700156869bac'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.16.7.linux-386.tar.gz'; 			sha256='5c0c8891fa88993f2193fbc9dd5cca6c250c89aa8c12bbaa382b6ff38139bcc3'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.16.7.linux-ppc64le.tar.gz'; 			sha256='03e02b2ac6dc1601203f335385b9bbe15a55677066d9a1a1280b5fcfa6ec4738'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.16.7.linux-s390x.tar.gz'; 			sha256='5f691c9551710ebb17bbda04389944aa7332f42ab28f92516a69fbd7860e7e9f'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 		sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 05 Aug 2021 21:40:34 GMT
ENV GOPATH=/go
# Thu, 05 Aug 2021 21:40:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Aug 2021 21:40:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 05 Aug 2021 21:40:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:276c935c592dc1b2a80709bfb684b8cadd019d62fed321da14653e74bc260bd2`  
		Last Modified: Thu, 22 Jul 2021 00:45:59 GMT  
		Size: 51.2 MB (51206749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74777b942e5ddcca1441a21360061ce9f880ebd5f5020bd1f8480c09ec3c9a1`  
		Last Modified: Thu, 22 Jul 2021 04:15:32 GMT  
		Size: 8.0 MB (7998524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f821b4d53bda0dd46941c09587233f0b5d34c76bd3efb4d2d0766dddea8f99`  
		Last Modified: Thu, 22 Jul 2021 04:15:33 GMT  
		Size: 10.3 MB (10339898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b349e22a93ae2ec7a8fb4830b9b80b272c758fbff384a0410f5c834c9c26a681`  
		Last Modified: Thu, 22 Jul 2021 04:16:00 GMT  
		Size: 53.4 MB (53437923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:479946c45602f49688fd89ae011dcae1ef8315e2d84dc6e4c3e2df15ea1f2534`  
		Last Modified: Thu, 22 Jul 2021 17:34:54 GMT  
		Size: 73.6 MB (73617644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d6df595cd4f368af75cbfde80508e683a7b064116742f6c36b709a3595e7fa`  
		Last Modified: Thu, 05 Aug 2021 22:04:52 GMT  
		Size: 103.1 MB (103086058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049984c13532b1816a2f80a192ca1175768e707ee9f9b28f9ad5cb9fb65d516f`  
		Last Modified: Thu, 05 Aug 2021 22:04:29 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; mips64le

```console
$ docker pull golang@sha256:835e7f82f6127351e6b1e72fd6753b3bb66be086a78a0e2f7b0baef13fb8074b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.5 MB (274478139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1332027ebd4c3a972158c143fe3974296e003b6a718a510b696c9c887e2ae3fd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:09:22 GMT
ADD file:1a6aa3d9fc5224e35958d4109d5bcb3afa5948beb85e45b91f46655fe8fadb2f in / 
# Thu, 22 Jul 2021 00:09:23 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 00:42:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 00:42:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 00:43:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 18:36:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 18:36:27 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Aug 2021 01:41:15 GMT
ENV GOLANG_VERSION=1.17
# Tue, 17 Aug 2021 01:51:02 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.17.linux-amd64.tar.gz'; 			sha256='6bf89fc4f5ad763871cf7eac80a2d594492de7a818303283f1366a7f6a30372d'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.linux-armv6l.tar.gz'; 			sha256='ae89d33f4e4acc222bdb04331933d5ece4ae71039812f6ccd7493cb3e8ddfb4e'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.linux-arm64.tar.gz'; 			sha256='01a9af009ada22122d3fcb9816049c1d21842524b38ef5d5a0e2ee4b26d7c3e7'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.linux-386.tar.gz'; 			sha256='c19e3227a6ac6329db91d1af77bbf239ccd760a259c16e6b9c932d527ff14848'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.linux-ppc64le.tar.gz'; 			sha256='ee84350114d532bf15f096198c675aafae9ff091dc4cc69eb49e1817ff94dbd7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.linux-s390x.tar.gz'; 			sha256='a50aaecf054f393575f969a9105d5c6864dd91afc5287d772449033fbafcf7e3'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.src.tar.gz'; 		sha256='3a70e5055509f347c0fb831ca07a2bf3b531068f349b14a3c652e9b5b67beb5d'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Tue, 17 Aug 2021 01:51:04 GMT
ENV GOPATH=/go
# Tue, 17 Aug 2021 01:51:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Aug 2021 01:51:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 17 Aug 2021 01:51:07 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:dfc6cf8967b24f7ad8c4469c3140cf3967000ae27e3b40b7c72fb89755953841`  
		Last Modified: Thu, 22 Jul 2021 00:15:25 GMT  
		Size: 49.1 MB (49080577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c97f1ec44468b6cf3c95775fd68ad34176e3f3f5b114e01ef45fda232435a0ee`  
		Last Modified: Thu, 22 Jul 2021 00:54:11 GMT  
		Size: 7.3 MB (7252390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5a98fef30417ecbf0d84d2f4e0a5d8c4c745505f4453d9d128eaabe85f0caa`  
		Last Modified: Thu, 22 Jul 2021 00:54:11 GMT  
		Size: 10.0 MB (10016296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d36b0ec1b127ef255da5d2ac89935eebf1177a48ee713fa2c190f0357961a9c`  
		Last Modified: Thu, 22 Jul 2021 00:55:01 GMT  
		Size: 50.8 MB (50844871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4efd8c3e0917726909d66a1120a3edfe62a1786d35c564dec6a6af02454cda92`  
		Last Modified: Thu, 22 Jul 2021 19:03:17 GMT  
		Size: 54.7 MB (54668722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f878c947395bd2398ad0266916f6da2b197179069d840390d1ecc4510f8b83b`  
		Last Modified: Tue, 17 Aug 2021 02:02:25 GMT  
		Size: 102.6 MB (102615158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470855b957b2ab5ea17c15a46502aba470b1c46bbb45910b3d389b6bdcbf96be`  
		Last Modified: Tue, 17 Aug 2021 02:01:15 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; ppc64le

```console
$ docker pull golang@sha256:f497dc3e6aaa05ffe3bd03b81ddd6f5e58c56b65ee36658531bc563aa03badbd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.4 MB (302395667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40ef9a9b1e06a169ad7690315a67a40d3aff5760143d9fa295b771c33e692a8e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:18:15 GMT
ADD file:e6b00a20c003d499ec3793592cb620a450afe5de34f408e897ae9ea6efde50ea in / 
# Thu, 22 Jul 2021 00:18:25 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 04:03:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 04:04:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 04:06:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 04:30:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Fri, 23 Jul 2021 04:30:58 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Aug 2021 22:49:01 GMT
ENV GOLANG_VERSION=1.16.7
# Thu, 05 Aug 2021 22:49:37 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.16.7.linux-amd64.tar.gz'; 			sha256='7fe7a73f55ba3e2285da36f8b085e5c0159e9564ef5f63ee0ed6b818ade8ef04'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.16.7.linux-armv6l.tar.gz'; 			sha256='b2973ceeae234866368baf9469fb7b9444857e50dc785ba879d98a0aa208a12b'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.16.7.linux-arm64.tar.gz'; 			sha256='63d6b53ecbd2b05c1f0e9903c92042663f2f68afdbb67f4d0d12700156869bac'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.16.7.linux-386.tar.gz'; 			sha256='5c0c8891fa88993f2193fbc9dd5cca6c250c89aa8c12bbaa382b6ff38139bcc3'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.16.7.linux-ppc64le.tar.gz'; 			sha256='03e02b2ac6dc1601203f335385b9bbe15a55677066d9a1a1280b5fcfa6ec4738'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.16.7.linux-s390x.tar.gz'; 			sha256='5f691c9551710ebb17bbda04389944aa7332f42ab28f92516a69fbd7860e7e9f'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.16.7.src.tar.gz'; 		sha256='1a9f2894d3d878729f7045072f30becebe243524cf2fce4e0a7b248b1e0654ac'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 05 Aug 2021 22:49:44 GMT
ENV GOPATH=/go
# Thu, 05 Aug 2021 22:49:46 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Aug 2021 22:49:51 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 05 Aug 2021 22:49:54 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fdbf50ea37550aa240918e3856b527a5dcc59fb570024ad98c902fe59e2ffd85`  
		Last Modified: Thu, 22 Jul 2021 00:27:11 GMT  
		Size: 54.2 MB (54182444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c4eb1cdb7dec331ac914405cf72cda55e246497aa6cdfce759e808d8b0ef32`  
		Last Modified: Thu, 22 Jul 2021 05:13:39 GMT  
		Size: 8.3 MB (8271846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1473db4da98c45802b5d0ee67cc543db64220182999ed71199a61f006246bb4`  
		Last Modified: Thu, 22 Jul 2021 05:13:37 GMT  
		Size: 10.7 MB (10727883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074eb7243d00a87169e9668977de9e6f8c1b4add7e5ee0b9a74e679a90f8abb3`  
		Last Modified: Thu, 22 Jul 2021 05:14:59 GMT  
		Size: 57.5 MB (57457626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7d28b1f45661e33c8c72a41565f5fa09f8856efaa0fc5a8eb90fc4532d5717`  
		Last Modified: Fri, 23 Jul 2021 04:47:39 GMT  
		Size: 73.7 MB (73659587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a48c1774a258c5a0eb2939ec9550e235d7d4d1177470f336af5a0f17cf5ea5`  
		Last Modified: Thu, 05 Aug 2021 23:01:57 GMT  
		Size: 98.1 MB (98096126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1cfb019bcd8bdd315c37a101ef4c259c8123a24e4448dd762628895fb3a976`  
		Last Modified: Thu, 05 Aug 2021 23:01:39 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-buster` - linux; s390x

```console
$ docker pull golang@sha256:58f8e3ddf3ad00e29e81f263efbb86a969b02fae230bf8dbe4a922ab3a707fad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280244463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ff4ea05acd96ff267f5da5584571b8354d18e391b0f531a1bd5b75eef2a0ed`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 22 Jul 2021 00:42:21 GMT
ADD file:0862dc2e420958057c0edfbacc39968850751ffdec84962ab8577b7787c5296f in / 
# Thu, 22 Jul 2021 00:42:26 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 01:11:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:11:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 01:12:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 21:21:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 21:21:32 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Aug 2021 02:03:42 GMT
ENV GOLANG_VERSION=1.17
# Tue, 17 Aug 2021 02:04:23 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	url=; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://dl.google.com/go/go1.17.linux-amd64.tar.gz'; 			sha256='6bf89fc4f5ad763871cf7eac80a2d594492de7a818303283f1366a7f6a30372d'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.linux-armv6l.tar.gz'; 			sha256='ae89d33f4e4acc222bdb04331933d5ece4ae71039812f6ccd7493cb3e8ddfb4e'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.linux-arm64.tar.gz'; 			sha256='01a9af009ada22122d3fcb9816049c1d21842524b38ef5d5a0e2ee4b26d7c3e7'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.linux-386.tar.gz'; 			sha256='c19e3227a6ac6329db91d1af77bbf239ccd760a259c16e6b9c932d527ff14848'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.linux-ppc64le.tar.gz'; 			sha256='ee84350114d532bf15f096198c675aafae9ff091dc4cc69eb49e1817ff94dbd7'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.linux-s390x.tar.gz'; 			sha256='a50aaecf054f393575f969a9105d5c6864dd91afc5287d772449033fbafcf7e3'; 			;; 		*) echo >&2 "error: unsupported architecture '$dpkgArch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.src.tar.gz'; 		sha256='3a70e5055509f347c0fb831ca07a2bf3b531068f349b14a3c652e9b5b67beb5d'; 		echo >&2; 		echo >&2 "warning: current architecture ($dpkgArch) does not have a corresponding Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc" --progress=dot:giga; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum --strict --check -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Tue, 17 Aug 2021 02:04:37 GMT
ENV GOPATH=/go
# Tue, 17 Aug 2021 02:04:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Aug 2021 02:04:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 17 Aug 2021 02:04:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8776c37054ddd28ba8fe526b8dbc08bf7b521ae9ddb8eacd008d05185571cde0`  
		Last Modified: Thu, 22 Jul 2021 00:47:50 GMT  
		Size: 49.0 MB (49003783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c06f635d71fe906f56e25278d5659aa940f095c1ecf199e41436e197534383a`  
		Last Modified: Thu, 22 Jul 2021 01:27:40 GMT  
		Size: 7.4 MB (7400582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f57129f34059279bed7373d2b35f16c94df2418b85c5ae20dc715f2e1999498`  
		Last Modified: Thu, 22 Jul 2021 01:27:41 GMT  
		Size: 9.9 MB (9883324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f6521600d1dbe8e9e84511427b15a7cb2dd42039504bb9679b6ed7e7ee0dca`  
		Last Modified: Thu, 22 Jul 2021 01:28:00 GMT  
		Size: 51.4 MB (51380867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1228c41a068ba9c3aca67ff810dadc0c8a62694a090ea82e610e8728cfbbb031`  
		Last Modified: Thu, 22 Jul 2021 21:28:50 GMT  
		Size: 56.8 MB (56817857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ccde3feaba6a3e15ff604b79d27ec18f603cbb7bb1d014d4524c51780e3794`  
		Last Modified: Tue, 17 Aug 2021 02:13:23 GMT  
		Size: 105.8 MB (105757896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:306e9f55e850bd6d772e4f5be3e3564db269731ea3a3e9aecbfeaca969348948`  
		Last Modified: Tue, 17 Aug 2021 02:13:09 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
