## `golang:buster`

```console
$ docker pull golang@sha256:202b7098b6bd5c91faacce750514a61e2dd2c31a93b419eca3bb0af3c409835b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `golang:buster` - linux; amd64

```console
$ docker pull golang@sha256:f64c8940473861d3de1b54182ba661b43a17984eeb0b29f53e7cbbc94b7ad649
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.9 MB (337872909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:042f6eeaba56a1cee79e8d009325d6cada09f42c9f3e0b7aa440c92fd090ad70`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:44:02 GMT
ADD file:259be79d94a2549a667ad08a093fe18f15a6c93d66a0723292f49294e31fc7a1 in / 
# Tue, 25 Oct 2022 01:44:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 09:25:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 09:25:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 09:25:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 00:49:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 00:49:26 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Oct 2022 00:49:26 GMT
ENV GOLANG_VERSION=1.19.2
# Wed, 26 Oct 2022 00:49:40 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.19.2.linux-amd64.tar.gz'; 			sha256='5e8c5a74fe6470dd7e055a461acda8bb4050ead8c2df70f227e3ff7d8eb7eeb6'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.19.2.linux-armv6l.tar.gz'; 			sha256='f3ccec7816ecd704ebafd130b08b8ad97c55402a8193a107b63e9de12ab90118'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.19.2.linux-arm64.tar.gz'; 			sha256='b62a8d9654436c67c14a0c91e931d50440541f09eb991a987536cb982903126d'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.19.2.linux-386.tar.gz'; 			sha256='ba8c97965e0856c69c9ca2c86f96bec5bb21de43e6533e25494bb211d85cda1b'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.19.2.linux-ppc64le.tar.gz'; 			sha256='37e1d4342f7103aeb9babeabe8c71ef3dba23db28db525071119e94b2aa21d7d'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.19.2.linux-s390x.tar.gz'; 			sha256='51b45dec41295215df17f78e67d1a373b9dda97a5e539bed440974da5ffc97de'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.2.src.tar.gz'; 		sha256='2ce930d70a931de660fdaf271d70192793b1b240272645bf0275779f6704df6b'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Wed, 26 Oct 2022 00:49:41 GMT
ENV GOPATH=/go
# Wed, 26 Oct 2022 00:49:41 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Oct 2022 00:49:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 26 Oct 2022 00:49:42 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fd31ec14dccdcda8f2472547f1a94ef0a23b8dabb764cd7b1d48aeee0afea7c8`  
		Last Modified: Tue, 25 Oct 2022 01:48:15 GMT  
		Size: 50.4 MB (50447742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6422bfa32650e77d346bbb40c6b2a0dc34c863e10cfb1a117e8da9796694cd`  
		Last Modified: Tue, 25 Oct 2022 09:48:47 GMT  
		Size: 7.9 MB (7858969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:335cbfc794fe106b207828e6c9d76fb72aa4631aad91b744e23442082275b8af`  
		Last Modified: Tue, 25 Oct 2022 09:48:47 GMT  
		Size: 10.0 MB (10001487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a348ba61fbef6dec66be0354c013afc02f0bba15b891b9625ac45bb007e9726`  
		Last Modified: Tue, 25 Oct 2022 09:49:04 GMT  
		Size: 51.8 MB (51843777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5858f738f60a61b19ca6dd0f1ccae27697bcde5edf908953104af97ec511ad6`  
		Last Modified: Wed, 26 Oct 2022 00:52:01 GMT  
		Size: 68.8 MB (68836764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b11426a1a5bce75bdfc459c47732f2ebe216e2a046e838a3672851db3f67784d`  
		Last Modified: Wed, 26 Oct 2022 00:52:10 GMT  
		Size: 148.9 MB (148884014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:967dda61ce15ef1594fb09a4701c7745401b0dd5d621075f7ebef0b06fb11954`  
		Last Modified: Wed, 26 Oct 2022 00:51:49 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:buster` - linux; arm variant v7

```console
$ docker pull golang@sha256:02bb8b2ae9a89d7cb833f503e2302c37894f8ab5e6cabe44cc77c87ca1f7ea41
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279796793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5776d6b8364b372fa9dc6692f6ff4323de8c0861f759a5ec629127a18f8c6260`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:59:00 GMT
ADD file:b16f07fda9b8beecd7c275565d0ed135fb298c712482766c8f0e40fac932130c in / 
# Tue, 04 Oct 2022 23:59:01 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:34:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:35:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Oct 2022 00:35:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 15:06:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 15:06:53 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 15:06:53 GMT
ENV GOLANG_VERSION=1.19.2
# Thu, 06 Oct 2022 15:07:19 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.19.2.linux-amd64.tar.gz'; 			sha256='5e8c5a74fe6470dd7e055a461acda8bb4050ead8c2df70f227e3ff7d8eb7eeb6'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.19.2.linux-armv6l.tar.gz'; 			sha256='f3ccec7816ecd704ebafd130b08b8ad97c55402a8193a107b63e9de12ab90118'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.19.2.linux-arm64.tar.gz'; 			sha256='b62a8d9654436c67c14a0c91e931d50440541f09eb991a987536cb982903126d'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.19.2.linux-386.tar.gz'; 			sha256='ba8c97965e0856c69c9ca2c86f96bec5bb21de43e6533e25494bb211d85cda1b'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.19.2.linux-ppc64le.tar.gz'; 			sha256='37e1d4342f7103aeb9babeabe8c71ef3dba23db28db525071119e94b2aa21d7d'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.19.2.linux-s390x.tar.gz'; 			sha256='51b45dec41295215df17f78e67d1a373b9dda97a5e539bed440974da5ffc97de'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.2.src.tar.gz'; 		sha256='2ce930d70a931de660fdaf271d70192793b1b240272645bf0275779f6704df6b'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Thu, 06 Oct 2022 15:07:19 GMT
ENV GOPATH=/go
# Thu, 06 Oct 2022 15:07:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 15:07:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 Oct 2022 15:07:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:bba3a5db4dfa403d6e1db947629616e80fb4514e2190e6aa1fb6a2c828c32491`  
		Last Modified: Wed, 05 Oct 2022 00:05:35 GMT  
		Size: 45.9 MB (45914973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0469c30b40a2c26072c228ab2795c38de425870b9ee85d29a32a2f50db3c4f`  
		Last Modified: Wed, 05 Oct 2022 00:55:03 GMT  
		Size: 7.1 MB (7145345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5315d494a34df967f8f4db548d0b40754c70678b9357188c65dc0b9cfee4f7e`  
		Last Modified: Wed, 05 Oct 2022 00:55:03 GMT  
		Size: 9.3 MB (9344666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317e83f2e93982c08cca0dc1dc3456b7bdfa7cdc43011e894195ad828de7550c`  
		Last Modified: Wed, 05 Oct 2022 00:55:25 GMT  
		Size: 47.4 MB (47363676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab668ebf56e30be1a14aeafc9fcbaa86742f28b8cc53fbab9cf3e115dc67724`  
		Last Modified: Thu, 06 Oct 2022 15:10:43 GMT  
		Size: 53.3 MB (53308707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc92bff8249452a9a307ce7912742003efa7d7ebae57975a84cc331630ec88d1`  
		Last Modified: Thu, 06 Oct 2022 15:10:54 GMT  
		Size: 116.7 MB (116719272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e7fce6dfc13b6e8a5ce01064185576f3594cbc49c6cd2e5060cbc020b433c80`  
		Last Modified: Thu, 06 Oct 2022 15:10:34 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:buster` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:4e1d7a82919e8b530c5134f8661138d197a201ea3e1f196c6698f00074332dee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.5 MB (296480498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31dfc2b65d8928d6fd6e4c6f5916beb24a24fdbeb41cb5ff8d91264a13442b43`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:54 GMT
ADD file:ef2ee78fb3eda698ebec33ff4b6dea672e03908b0f8630a28acb33ec9a7c3e13 in / 
# Tue, 04 Oct 2022 23:44:55 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:24:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:24:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Oct 2022 00:24:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 17:11:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 17:11:19 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 17:11:20 GMT
ENV GOLANG_VERSION=1.19.2
# Wed, 05 Oct 2022 17:11:33 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.19.2.linux-amd64.tar.gz'; 			sha256='5e8c5a74fe6470dd7e055a461acda8bb4050ead8c2df70f227e3ff7d8eb7eeb6'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.19.2.linux-armv6l.tar.gz'; 			sha256='f3ccec7816ecd704ebafd130b08b8ad97c55402a8193a107b63e9de12ab90118'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.19.2.linux-arm64.tar.gz'; 			sha256='b62a8d9654436c67c14a0c91e931d50440541f09eb991a987536cb982903126d'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.19.2.linux-386.tar.gz'; 			sha256='ba8c97965e0856c69c9ca2c86f96bec5bb21de43e6533e25494bb211d85cda1b'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.19.2.linux-ppc64le.tar.gz'; 			sha256='37e1d4342f7103aeb9babeabe8c71ef3dba23db28db525071119e94b2aa21d7d'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.19.2.linux-s390x.tar.gz'; 			sha256='51b45dec41295215df17f78e67d1a373b9dda97a5e539bed440974da5ffc97de'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.2.src.tar.gz'; 		sha256='2ce930d70a931de660fdaf271d70192793b1b240272645bf0275779f6704df6b'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Wed, 05 Oct 2022 17:11:35 GMT
ENV GOPATH=/go
# Wed, 05 Oct 2022 17:11:36 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 17:11:37 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 05 Oct 2022 17:11:38 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:504dcdd9b4a0035dba7a55a5312cf594c3d22fb99b7bf676d397c464db919009`  
		Last Modified: Tue, 04 Oct 2022 23:50:47 GMT  
		Size: 49.2 MB (49228885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ae492f07ea828401b80eb34c8c630b72cb66cac155b003e81ab2921dc57f3d`  
		Last Modified: Wed, 05 Oct 2022 00:38:37 GMT  
		Size: 7.7 MB (7722031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c91e11c5a0db8322590ddbb61600624fdd82d3d6174d1de01c30be3e7ca535`  
		Last Modified: Wed, 05 Oct 2022 00:38:37 GMT  
		Size: 9.8 MB (9769003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647de18a9400fa5e9ba5c0c5aaacd374b6728cbf14527e0ac59947e0b864af27`  
		Last Modified: Wed, 05 Oct 2022 00:38:55 GMT  
		Size: 52.2 MB (52175488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ea249f502eb8e1c55d0067eb17d4570d3c5085d77d20eb46a59a9827fe14ce`  
		Last Modified: Wed, 05 Oct 2022 17:14:38 GMT  
		Size: 62.5 MB (62476351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f089915102742517051f01e55a9ef376973d23c1907c1f71141b37e3a82dde06`  
		Last Modified: Wed, 05 Oct 2022 17:14:46 GMT  
		Size: 115.1 MB (115108614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e23ea2a5ea48ce8347570bbe2cf7ceca0c93c468dfaf215e534b41758fb66b0`  
		Last Modified: Wed, 05 Oct 2022 17:14:29 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:buster` - linux; 386

```console
$ docker pull golang@sha256:f772493b4bb142a3eeb5f267a4ed88ec354026fb4da70f889f5525e244d37532
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.3 MB (316313037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0bf67af38fe6e1a4b1adfa50e519efa3da846e2ebc966e16ee48cd68678c7cc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 02:22:47 GMT
ADD file:7e14d4afa5499129c959c5ae5dc270e2fa04659c2c9b0527094cda3494c02d0f in / 
# Tue, 25 Oct 2022 02:22:47 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 05:16:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 05:16:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 05:17:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 18:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 18:23:25 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Oct 2022 18:23:25 GMT
ENV GOLANG_VERSION=1.19.2
# Tue, 25 Oct 2022 18:23:40 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.19.2.linux-amd64.tar.gz'; 			sha256='5e8c5a74fe6470dd7e055a461acda8bb4050ead8c2df70f227e3ff7d8eb7eeb6'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.19.2.linux-armv6l.tar.gz'; 			sha256='f3ccec7816ecd704ebafd130b08b8ad97c55402a8193a107b63e9de12ab90118'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.19.2.linux-arm64.tar.gz'; 			sha256='b62a8d9654436c67c14a0c91e931d50440541f09eb991a987536cb982903126d'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.19.2.linux-386.tar.gz'; 			sha256='ba8c97965e0856c69c9ca2c86f96bec5bb21de43e6533e25494bb211d85cda1b'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.19.2.linux-ppc64le.tar.gz'; 			sha256='37e1d4342f7103aeb9babeabe8c71ef3dba23db28db525071119e94b2aa21d7d'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.19.2.linux-s390x.tar.gz'; 			sha256='51b45dec41295215df17f78e67d1a373b9dda97a5e539bed440974da5ffc97de'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.2.src.tar.gz'; 		sha256='2ce930d70a931de660fdaf271d70192793b1b240272645bf0275779f6704df6b'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		go version
# Tue, 25 Oct 2022 18:23:41 GMT
ENV GOPATH=/go
# Tue, 25 Oct 2022 18:23:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Oct 2022 18:23:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 25 Oct 2022 18:23:44 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:76a731c42f665e7334a622f65117ef9389e97a878b7c74bb4a10dfe9cdb296c6`  
		Last Modified: Tue, 25 Oct 2022 02:28:50 GMT  
		Size: 51.2 MB (51207943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee1fc3722feabf994120ab8f7d4abab754206d1ca425b7274ce1db428f7a651`  
		Last Modified: Tue, 25 Oct 2022 05:28:54 GMT  
		Size: 8.0 MB (8025806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2019db6202a77d9f3c2e49a64c766b8b67d4290e0e66e1480fd8c576078914b2`  
		Last Modified: Tue, 25 Oct 2022 05:28:54 GMT  
		Size: 10.1 MB (10128021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79afff7d2fb8bbf10afd83b8f08278ed493a12e50a8262a18a1b3fc227667ec4`  
		Last Modified: Tue, 25 Oct 2022 05:29:13 GMT  
		Size: 53.4 MB (53442950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb3c9537515f3b53b865ac72ac8d184e3bfdd7490ddb0866939c4f03e9c806e`  
		Last Modified: Tue, 25 Oct 2022 18:27:00 GMT  
		Size: 73.5 MB (73480983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc1066a86bc44707b5599a1b845605dd62c7d4339e8634f7077354d98556779`  
		Last Modified: Tue, 25 Oct 2022 18:27:05 GMT  
		Size: 120.0 MB (120027208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a2103d7c9d175520664305a5184e1457945a9b8c99601256339892ccc3c680`  
		Last Modified: Tue, 25 Oct 2022 18:26:49 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
