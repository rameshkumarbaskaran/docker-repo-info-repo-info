## `golang:1-stretch`

```console
$ docker pull golang@sha256:db367b3ca1b77ee802ff8319cf66650190fc0fcef9d0985c394ace6b805389fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `golang:1-stretch` - linux; amd64

```console
$ docker pull golang@sha256:8df354274dab52d9b1d555e07e2b2d891c8fb41a6449976425609c471f1c594c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.4 MB (303410441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ccc740958817b0ce5a25d6fe7fb784de42e14d90f1917b1ed38400b7c7102a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:23:33 GMT
ADD file:835effce8521d3a6cb00dc8bb358711e7a6ba1fd057b798681d9e006825dd3c1 in / 
# Fri, 03 Sep 2021 01:23:33 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 06:36:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 06:36:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Sep 2021 06:36:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Sep 2021 08:29:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Sep 2021 08:29:25 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Sep 2021 21:20:41 GMT
ENV GOLANG_VERSION=1.17.1
# Thu, 09 Sep 2021 21:21:00 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.1.linux-amd64.tar.gz'; 			sha256='dab7d9c34361dc21ec237d584590d72500652e7c909bf082758fb63064fca0ef'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.1.linux-armv6l.tar.gz'; 			sha256='ed3e4dbc9b80353f6482c441d65b51808290e94ff1d15d56da5f4a7be7353758'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.1.linux-arm64.tar.gz'; 			sha256='53b29236fa03ed862670a5e5e2ab2439a2dc288fe61544aa392062104ac0128c'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.1.linux-386.tar.gz'; 			sha256='e60bb44046f424ba2cc47db7b183079b5add2f8cfa6887daf45bf2f317cc2f53'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.1.linux-ppc64le.tar.gz'; 			sha256='df4fa945512c3b472cf3d2dcb2e4ae5b34819607bc63f3223f5bc0c17b637dd0'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.1.linux-s390x.tar.gz'; 			sha256='f770b72e1e1281239b12b64825f87a928a1788943c7f09cac7f28985ef2cf692'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.1.src.tar.gz'; 		sha256='49dc08339770acd5613312db8c141eaf61779995577b89d93b541ef83067e5b1'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 09 Sep 2021 21:21:01 GMT
ENV GOPATH=/go
# Thu, 09 Sep 2021 21:21:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Sep 2021 21:21:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 09 Sep 2021 21:21:02 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1c05d83e138cea8cb6ddd17442ab2138423db80e58408d93059f2ea25065952e`  
		Last Modified: Fri, 03 Sep 2021 01:31:39 GMT  
		Size: 45.4 MB (45379797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:394ee1959bac9492a9fc64334844549eccd4274280678d81d6b5b19af703e2a6`  
		Last Modified: Fri, 03 Sep 2021 06:42:58 GMT  
		Size: 11.3 MB (11295763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5f175d1abbc6d4a7774bd2912a927aa78b90fb04fb43d591e3dda317c9bb96`  
		Last Modified: Fri, 03 Sep 2021 06:42:57 GMT  
		Size: 4.3 MB (4342391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7885553ee256f7f9d1dd3016c0fd0c72fcd46217439371e3e1f610af0d159004`  
		Last Modified: Fri, 03 Sep 2021 06:43:17 GMT  
		Size: 49.8 MB (49761954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884ea03617543fd3eb6727d5dab474bcb8b11b5c36ff2783d442f32550770ff2`  
		Last Modified: Sat, 04 Sep 2021 08:33:08 GMT  
		Size: 57.8 MB (57846200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c1f6e5eb2db8cc657e23062f2bf0e700e5665f73a426fee8f54368059ce7305`  
		Last Modified: Thu, 09 Sep 2021 21:31:47 GMT  
		Size: 134.8 MB (134784181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75f28318331b619092cf5fa49b8468adac1ff7540a72d6dca084c55c6c97982`  
		Last Modified: Thu, 09 Sep 2021 21:31:28 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-stretch` - linux; arm variant v7

```console
$ docker pull golang@sha256:db404cbab7516e1dcbd5364959797c6a375b5e99296265d27c726061ba613912
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.4 MB (251369064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f7469e48ffd93a33fbc93eadfd673e7b4e789ca6ee0b7d3e6e32afc5cc9080`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 01:04:44 GMT
ADD file:f3526ca980237b2ca5289ca7a6c67760fc5726ce3c325de10f3f3111c1d4bdcd in / 
# Fri, 03 Sep 2021 01:04:45 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 03:03:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 03:03:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Sep 2021 03:04:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Sep 2021 07:16:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Sep 2021 07:16:18 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Sep 2021 22:45:02 GMT
ENV GOLANG_VERSION=1.17.1
# Thu, 09 Sep 2021 22:45:35 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.1.linux-amd64.tar.gz'; 			sha256='dab7d9c34361dc21ec237d584590d72500652e7c909bf082758fb63064fca0ef'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.1.linux-armv6l.tar.gz'; 			sha256='ed3e4dbc9b80353f6482c441d65b51808290e94ff1d15d56da5f4a7be7353758'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.1.linux-arm64.tar.gz'; 			sha256='53b29236fa03ed862670a5e5e2ab2439a2dc288fe61544aa392062104ac0128c'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.1.linux-386.tar.gz'; 			sha256='e60bb44046f424ba2cc47db7b183079b5add2f8cfa6887daf45bf2f317cc2f53'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.1.linux-ppc64le.tar.gz'; 			sha256='df4fa945512c3b472cf3d2dcb2e4ae5b34819607bc63f3223f5bc0c17b637dd0'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.1.linux-s390x.tar.gz'; 			sha256='f770b72e1e1281239b12b64825f87a928a1788943c7f09cac7f28985ef2cf692'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.1.src.tar.gz'; 		sha256='49dc08339770acd5613312db8c141eaf61779995577b89d93b541ef83067e5b1'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 09 Sep 2021 22:45:37 GMT
ENV GOPATH=/go
# Thu, 09 Sep 2021 22:45:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Sep 2021 22:45:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 09 Sep 2021 22:45:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:aba3565275cf0ab544dbd3d27fb468b4682c0273b64b5f3d8c8fe06ca3467237`  
		Last Modified: Fri, 03 Sep 2021 01:21:57 GMT  
		Size: 42.1 MB (42119584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d7b8704af020029979f5a4bfc12eaea904235f452d75b61476aa90807ec20b`  
		Last Modified: Fri, 03 Sep 2021 03:22:05 GMT  
		Size: 10.0 MB (9951651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef77f0ed56b31ff8d57db5fd7149505dac04ef41f4919d6a59ed5e3725a6f4e`  
		Last Modified: Fri, 03 Sep 2021 03:22:03 GMT  
		Size: 3.9 MB (3921218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:612339c5de82d58230628e90ab66882406b5153ad5eecc07c42f9418c7404e11`  
		Last Modified: Fri, 03 Sep 2021 03:22:49 GMT  
		Size: 46.1 MB (46125736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce755d4896eddcf3862aeddd1b543efd3675d77600f0c1fb2f6663dff91dbd4a`  
		Last Modified: Sat, 04 Sep 2021 07:26:34 GMT  
		Size: 46.2 MB (46178469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbaef597b136f17ba2ffac7a3feb13ca4520af51f1f4b5d10ec8ceb45dfa155`  
		Last Modified: Thu, 09 Sep 2021 23:08:36 GMT  
		Size: 103.1 MB (103072250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2803420e25a94d0e69df10f14fb8896a623d63cc244740872f4a71c1bece1d7`  
		Last Modified: Thu, 09 Sep 2021 23:07:28 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-stretch` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:c4c7531da89ef722c855ee68a1df21a4fd4ec7219888e7b67425ad0980efa317
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257073609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d6f8f19c8eaf998fa3e2bcd609f809cded5b4672b1a0a2c40c047d0dba1e2f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 28 Sep 2021 01:43:10 GMT
ADD file:d66cac067d9b02a4946e6816144b6c89b971f95947a48715a50600a63d153b56 in / 
# Tue, 28 Sep 2021 01:43:10 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 02:20:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 02:20:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 28 Sep 2021 02:20:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 16:32:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 16:32:05 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Sep 2021 16:32:05 GMT
ENV GOLANG_VERSION=1.17.1
# Tue, 28 Sep 2021 16:32:18 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.1.linux-amd64.tar.gz'; 			sha256='dab7d9c34361dc21ec237d584590d72500652e7c909bf082758fb63064fca0ef'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.1.linux-armv6l.tar.gz'; 			sha256='ed3e4dbc9b80353f6482c441d65b51808290e94ff1d15d56da5f4a7be7353758'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.1.linux-arm64.tar.gz'; 			sha256='53b29236fa03ed862670a5e5e2ab2439a2dc288fe61544aa392062104ac0128c'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.1.linux-386.tar.gz'; 			sha256='e60bb44046f424ba2cc47db7b183079b5add2f8cfa6887daf45bf2f317cc2f53'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.1.linux-ppc64le.tar.gz'; 			sha256='df4fa945512c3b472cf3d2dcb2e4ae5b34819607bc63f3223f5bc0c17b637dd0'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.1.linux-s390x.tar.gz'; 			sha256='f770b72e1e1281239b12b64825f87a928a1788943c7f09cac7f28985ef2cf692'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.1.src.tar.gz'; 		sha256='49dc08339770acd5613312db8c141eaf61779995577b89d93b541ef83067e5b1'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Tue, 28 Sep 2021 16:32:19 GMT
ENV GOPATH=/go
# Tue, 28 Sep 2021 16:32:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Sep 2021 16:32:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 28 Sep 2021 16:32:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7b4ff8ad8c828f0855329495e1260f28de7fc1e828e3339b7dddc2d116d19742`  
		Last Modified: Tue, 28 Sep 2021 01:52:24 GMT  
		Size: 43.2 MB (43176860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:056e66b20944d4cb1ecbb1744d2851e6e3f89c80e9db3afff03b3fc1c1291768`  
		Last Modified: Tue, 28 Sep 2021 02:28:21 GMT  
		Size: 10.2 MB (10216473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac70c4411ef34b85e9e038bdd0e1c5fb4b27ce5be304cdb9479fe829e2ab9886`  
		Last Modified: Tue, 28 Sep 2021 02:28:19 GMT  
		Size: 4.1 MB (4096542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65cdaa18192aee6f9c254882a3a7f4e57f28681ee263e9fd155fefcd6d9a7e7f`  
		Last Modified: Tue, 28 Sep 2021 02:28:40 GMT  
		Size: 47.7 MB (47737758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c408009c18784fff2e5117c0689206df56c686baf86350290cd379321788eb27`  
		Last Modified: Tue, 28 Sep 2021 16:36:53 GMT  
		Size: 49.2 MB (49238894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f113080e8906878d8a758b9cd1f7c3a60d7ba8b558c170b374ea35fc88cec2f6`  
		Last Modified: Tue, 28 Sep 2021 16:37:01 GMT  
		Size: 102.6 MB (102606926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c2a2a6a0ea47102529b4d755c10511dfab6fb8568f9a5069f9b011cfe97257`  
		Last Modified: Tue, 28 Sep 2021 16:36:45 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-stretch` - linux; 386

```console
$ docker pull golang@sha256:121e753c4f925e235f79fd63cf031f431aec5524f72926c2b2f9d5d645dc57f1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281251847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af581f178f3696532ce9510c786f3ebed1af45895e9e7dc5748d3a58b112207b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Sep 2021 00:42:30 GMT
ADD file:46f32d47386428deefe487caf3a07dcbb3fe2f2e89abd3b63cbe7e9d31444ec6 in / 
# Fri, 03 Sep 2021 00:42:30 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 01:15:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 01:15:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Sep 2021 01:16:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 21:48:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 21:48:05 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Sep 2021 20:39:59 GMT
ENV GOLANG_VERSION=1.17.1
# Thu, 09 Sep 2021 20:40:13 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.1.linux-amd64.tar.gz'; 			sha256='dab7d9c34361dc21ec237d584590d72500652e7c909bf082758fb63064fca0ef'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.1.linux-armv6l.tar.gz'; 			sha256='ed3e4dbc9b80353f6482c441d65b51808290e94ff1d15d56da5f4a7be7353758'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.1.linux-arm64.tar.gz'; 			sha256='53b29236fa03ed862670a5e5e2ab2439a2dc288fe61544aa392062104ac0128c'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.1.linux-386.tar.gz'; 			sha256='e60bb44046f424ba2cc47db7b183079b5add2f8cfa6887daf45bf2f317cc2f53'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.1.linux-ppc64le.tar.gz'; 			sha256='df4fa945512c3b472cf3d2dcb2e4ae5b34819607bc63f3223f5bc0c17b637dd0'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.1.linux-s390x.tar.gz'; 			sha256='f770b72e1e1281239b12b64825f87a928a1788943c7f09cac7f28985ef2cf692'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.1.src.tar.gz'; 		sha256='49dc08339770acd5613312db8c141eaf61779995577b89d93b541ef83067e5b1'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 09 Sep 2021 20:40:14 GMT
ENV GOPATH=/go
# Thu, 09 Sep 2021 20:40:15 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Sep 2021 20:40:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 09 Sep 2021 20:40:16 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:dadb58ce47b39e4093a503cf3b5a3fdb91180e4b16e14c1146b7bb865336d6f5`  
		Last Modified: Fri, 03 Sep 2021 00:52:52 GMT  
		Size: 46.1 MB (46097308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd444f00c798bfd4f9e617154309c372e8d36842dd1b1941d71becd772ddfcc`  
		Last Modified: Fri, 03 Sep 2021 01:23:40 GMT  
		Size: 11.4 MB (11353014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0571d1af33e8ba8e01d8c5f2ff9b4e4a3bd4bd88c459d958bfaa57077a0a3f6a`  
		Last Modified: Fri, 03 Sep 2021 01:23:39 GMT  
		Size: 4.6 MB (4564992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8dcaa4b267350835d07fbb9cd12470a43123a18957bf035ad503417f9fe38ef`  
		Last Modified: Fri, 03 Sep 2021 01:24:06 GMT  
		Size: 51.3 MB (51265099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5f5cc182bf0b89b25d60c6bbeb91b8718f8bc36862110778e66192c2c09c25`  
		Last Modified: Fri, 03 Sep 2021 21:54:08 GMT  
		Size: 62.4 MB (62372098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7478cc7f88744a0a3a2cc0b017784f5c61ef82417dd15ff94a389831db2d20b8`  
		Last Modified: Thu, 09 Sep 2021 20:59:48 GMT  
		Size: 105.6 MB (105599181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab6fba124938a31eadbd3a32ab50b94999fe7ee0b8f8efc26128553656a0420`  
		Last Modified: Thu, 09 Sep 2021 20:59:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
