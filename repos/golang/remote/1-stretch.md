## `golang:1-stretch`

```console
$ docker pull golang@sha256:2b6bc1dc2c0872412e6a544802000dab978067cb6036d07aece73e0eb0edf45c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `golang:1-stretch` - linux; amd64

```console
$ docker pull golang@sha256:29c108eea53af94b0ebec5db0972407813783d99ef344f81c048b2a31f4ce158
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.4 MB (303437905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9851194393abd3fcd1f1386903bafe8fcf5a638a4580ef228e322af9465402a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:22:28 GMT
ADD file:d7365dd9cf34b10ca189f85c95c21a0c33e44092f85ffb5884d5e737fb0b9be1 in / 
# Wed, 17 Nov 2021 02:22:28 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:19:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 03:19:29 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Nov 2021 03:19:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 09:52:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 09:52:39 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Nov 2021 09:52:39 GMT
ENV GOLANG_VERSION=1.17.3
# Tue, 30 Nov 2021 04:21:36 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.3.linux-amd64.tar.gz'; 			sha256='550f9845451c0c94be679faf116291e7807a8d78b43149f9506c1b15eb89008c'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.3.linux-armv6l.tar.gz'; 			sha256='aa0d5516c8bd61654990916274d27491cfa229d322475502b247a8dc885adec5'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.3.linux-arm64.tar.gz'; 			sha256='06f505c8d27203f78706ad04e47050b49092f1b06dc9ac4fbee4f0e4d015c8d4'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.3.linux-386.tar.gz'; 			sha256='982487a0264626950c635c5e185df68ecaadcca1361956207578d661a7b03bee'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.3.linux-ppc64le.tar.gz'; 			sha256='b821ff58d088c61adc5d7376179a342f325d8715a06abdeb6974f6450663ee60'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.3.linux-s390x.tar.gz'; 			sha256='7d1727e08fef295f48aed2b8124a07e3752e77aea747fcc7aeb8892b8e2f2ad2'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Tue, 30 Nov 2021 04:21:37 GMT
ENV GOPATH=/go
# Tue, 30 Nov 2021 04:21:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Nov 2021 04:21:38 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 30 Nov 2021 04:21:38 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:200cae5c9d88bb9cf1dd3fcfb831d671403f078d2310416fa3b304337d8279c0`  
		Last Modified: Wed, 17 Nov 2021 02:29:09 GMT  
		Size: 45.4 MB (45380444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:047156b8adafd241846cd5539cebd45e6e28fe1bd818cd654a0124cef61d4cb2`  
		Last Modified: Wed, 17 Nov 2021 03:27:27 GMT  
		Size: 11.3 MB (11301447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cbf304dd51feb48b321b93ae5b8a5a6ca55c23b51a8dc0d9642c3c3b5081a7`  
		Last Modified: Wed, 17 Nov 2021 03:27:26 GMT  
		Size: 4.3 MB (4342326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6e9db633dd66ac91ed2df32c5900c5a1ae82b58cc9261fd240913743d283ca`  
		Last Modified: Wed, 17 Nov 2021 03:27:45 GMT  
		Size: 49.8 MB (49762330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:725d9168d002fda2b398fba4873c623abf7509249b7f35e270fc32f245aa70ab`  
		Last Modified: Thu, 18 Nov 2021 09:56:29 GMT  
		Size: 57.8 MB (57846310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5026ca1eec7a5168c1d7daee8823138ccc1e3251b1a5d8d03bad823ebe961219`  
		Last Modified: Tue, 30 Nov 2021 04:35:46 GMT  
		Size: 134.8 MB (134804892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27003be93baa62554d8dd131889159190462bc632b21e6e80968427822ba610f`  
		Last Modified: Tue, 30 Nov 2021 04:35:20 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-stretch` - linux; arm variant v7

```console
$ docker pull golang@sha256:f31125e8d66dba88953c73ddc386945b00afbd51f3b2c040ed2d0b7304ef1ace
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.4 MB (251384083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb2b860d425aa2075453af5698876b830c8c18050dca9944f29112bfe41e97ec`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:04:57 GMT
ADD file:61da3fcef3aea99b4927189cfcb823a65b0e911a3f4436e44ea84a57a7919ff3 in / 
# Wed, 17 Nov 2021 02:04:58 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:54:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 02:54:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Nov 2021 02:55:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 15:24:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Nov 2021 15:24:14 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Nov 2021 15:24:14 GMT
ENV GOLANG_VERSION=1.17.3
# Tue, 30 Nov 2021 04:10:17 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.3.linux-amd64.tar.gz'; 			sha256='550f9845451c0c94be679faf116291e7807a8d78b43149f9506c1b15eb89008c'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.3.linux-armv6l.tar.gz'; 			sha256='aa0d5516c8bd61654990916274d27491cfa229d322475502b247a8dc885adec5'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.3.linux-arm64.tar.gz'; 			sha256='06f505c8d27203f78706ad04e47050b49092f1b06dc9ac4fbee4f0e4d015c8d4'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.3.linux-386.tar.gz'; 			sha256='982487a0264626950c635c5e185df68ecaadcca1361956207578d661a7b03bee'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.3.linux-ppc64le.tar.gz'; 			sha256='b821ff58d088c61adc5d7376179a342f325d8715a06abdeb6974f6450663ee60'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.3.linux-s390x.tar.gz'; 			sha256='7d1727e08fef295f48aed2b8124a07e3752e77aea747fcc7aeb8892b8e2f2ad2'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Tue, 30 Nov 2021 04:10:18 GMT
ENV GOPATH=/go
# Tue, 30 Nov 2021 04:10:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Nov 2021 04:10:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 30 Nov 2021 04:10:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e4d54b576c2fcdd259e57bac14c4e1a2623f6e5dc9a0b1facaed7fe59d891e86`  
		Last Modified: Wed, 17 Nov 2021 02:22:03 GMT  
		Size: 42.1 MB (42116868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf04dd2447fcded30a4c9a8d7a054ccb2e4c4db4118989ea05bf2e56d60a8924`  
		Last Modified: Wed, 17 Nov 2021 03:14:24 GMT  
		Size: 10.0 MB (9956153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b37c8e78d6ca4f8e5467e0ec7ef61eef6101e99c8154472df98aa34159f5974`  
		Last Modified: Wed, 17 Nov 2021 03:14:21 GMT  
		Size: 3.9 MB (3921214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20fcf28009119cc468ce87b98d583e8c51d3703937d10d502a704f1032bc2b26`  
		Last Modified: Wed, 17 Nov 2021 03:15:08 GMT  
		Size: 46.1 MB (46126162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ea826817c912b29536d6dd682f04ca258bb0db507af9fed07c98e3ae86eccf`  
		Last Modified: Thu, 18 Nov 2021 15:34:33 GMT  
		Size: 46.2 MB (46178466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02e20ebeb21c98086f894986451fa9f924be35a7b117a11c22633ed8cfd28219`  
		Last Modified: Tue, 30 Nov 2021 04:33:11 GMT  
		Size: 103.1 MB (103085064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:208e06bb56640406a9d593cecadafc8c288eb086c9bbce725768eb4608ae001c`  
		Last Modified: Tue, 30 Nov 2021 04:32:04 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-stretch` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:083ae82263bc375ae48547bbe0b4727698400531c6032400cdf68c2afec661eb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.6 MB (256630454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf46251a22999cc9bf6eba952fdca0790584e9998ddd23c7a897f873c32871d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 08:10:09 GMT
ADD file:7be59c7e3b187d010c0e8625e45324f421a21518258e6bd35bab6e0e86c9494c in / 
# Thu, 02 Dec 2021 08:10:10 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:57:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:58:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 09:58:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 05:07:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 05:07:46 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 05:07:47 GMT
ENV GOLANG_VERSION=1.17.3
# Fri, 03 Dec 2021 05:08:00 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.3.linux-amd64.tar.gz'; 			sha256='550f9845451c0c94be679faf116291e7807a8d78b43149f9506c1b15eb89008c'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.3.linux-armv6l.tar.gz'; 			sha256='aa0d5516c8bd61654990916274d27491cfa229d322475502b247a8dc885adec5'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.3.linux-arm64.tar.gz'; 			sha256='06f505c8d27203f78706ad04e47050b49092f1b06dc9ac4fbee4f0e4d015c8d4'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.3.linux-386.tar.gz'; 			sha256='982487a0264626950c635c5e185df68ecaadcca1361956207578d661a7b03bee'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.3.linux-ppc64le.tar.gz'; 			sha256='b821ff58d088c61adc5d7376179a342f325d8715a06abdeb6974f6450663ee60'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.3.linux-s390x.tar.gz'; 			sha256='7d1727e08fef295f48aed2b8124a07e3752e77aea747fcc7aeb8892b8e2f2ad2'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 03 Dec 2021 05:08:01 GMT
ENV GOPATH=/go
# Fri, 03 Dec 2021 05:08:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 05:08:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 03 Dec 2021 05:08:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6965f119641a6f16b55da01b7c12884960366228a181268b0bf7d0b7d50b2336`  
		Last Modified: Thu, 02 Dec 2021 08:44:30 GMT  
		Size: 43.2 MB (43173684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e211a2e7bbb27084e1f8cd62281719dc9d90e3ddb76b862e471b1cde61512cb`  
		Last Modified: Thu, 02 Dec 2021 10:08:36 GMT  
		Size: 10.2 MB (10216757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca410b1e11dc0ad76bc18c383eafa45a44c94916e27e4f327bc75a9373a250ca`  
		Last Modified: Thu, 02 Dec 2021 10:08:34 GMT  
		Size: 3.9 MB (3873863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c7b6f285f6115be3423f6435cf3cb41ad88d3e8e284f342de24037cc5c1824`  
		Last Modified: Thu, 02 Dec 2021 10:08:54 GMT  
		Size: 47.7 MB (47735220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfe8892c3ec2bab9f6ea439daca3fde4c3db161dc383e262e9af0d799b6697bb`  
		Last Modified: Fri, 03 Dec 2021 05:12:11 GMT  
		Size: 49.0 MB (49005963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad9d437926715223f678b5a4f95d159cc84da1531d89546dd3fc38cb450c4c4`  
		Last Modified: Fri, 03 Dec 2021 05:12:19 GMT  
		Size: 102.6 MB (102624842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb847522642a0f43ec1f4d6337a49f5d8ce46a611be77f2b9c1ed6cedb67d97`  
		Last Modified: Fri, 03 Dec 2021 05:12:04 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-stretch` - linux; 386

```console
$ docker pull golang@sha256:15479adfe46a3c9c94e6af89412e25f925b5a5aaa96df16e640a20216b7851e7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281276464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e5288575f7d2a6de4c42fbde71ae56a42b2ab7dc58a314b170d5de4d743181d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 02:42:27 GMT
ADD file:7211d8cf4427f9effab1662b9a54e89548974bde8e4162ccd44fddbc57024912 in / 
# Thu, 02 Dec 2021 02:42:27 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:16:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:16:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:17:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 04:44:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Dec 2021 04:44:51 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 04:44:52 GMT
ENV GOLANG_VERSION=1.17.3
# Fri, 03 Dec 2021 04:45:12 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.3.linux-amd64.tar.gz'; 			sha256='550f9845451c0c94be679faf116291e7807a8d78b43149f9506c1b15eb89008c'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.3.linux-armv6l.tar.gz'; 			sha256='aa0d5516c8bd61654990916274d27491cfa229d322475502b247a8dc885adec5'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.3.linux-arm64.tar.gz'; 			sha256='06f505c8d27203f78706ad04e47050b49092f1b06dc9ac4fbee4f0e4d015c8d4'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.3.linux-386.tar.gz'; 			sha256='982487a0264626950c635c5e185df68ecaadcca1361956207578d661a7b03bee'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.3.linux-ppc64le.tar.gz'; 			sha256='b821ff58d088c61adc5d7376179a342f325d8715a06abdeb6974f6450663ee60'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.3.linux-s390x.tar.gz'; 			sha256='7d1727e08fef295f48aed2b8124a07e3752e77aea747fcc7aeb8892b8e2f2ad2'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.3.src.tar.gz'; 		sha256='705c64251e5b25d5d55ede1039c6aa22bea40a7a931d14c370339853643c3df0'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				go install std; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 03 Dec 2021 04:45:13 GMT
ENV GOPATH=/go
# Fri, 03 Dec 2021 04:45:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 03 Dec 2021 04:45:15 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 03 Dec 2021 04:45:15 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8450ec7364298e2205fbbb540c3ebcbfe46324826539d90ea2e28eeec0bec114`  
		Last Modified: Thu, 02 Dec 2021 02:52:39 GMT  
		Size: 46.1 MB (46097889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae41b4dcbaba225a7711cee1762ef03e55d931f9b8ae39653c61d413766c74e2`  
		Last Modified: Thu, 02 Dec 2021 03:25:15 GMT  
		Size: 11.4 MB (11359074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4378944bb911d45fda5ea1e6a9d56bf6be60774251aea45049160deba235176`  
		Last Modified: Thu, 02 Dec 2021 03:25:13 GMT  
		Size: 4.6 MB (4564943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd039a786e792e776d9ad9ebbe0bb3444c8c7c458676a67bf483791c04408b6`  
		Last Modified: Thu, 02 Dec 2021 03:25:38 GMT  
		Size: 51.3 MB (51264993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1616b0d62ef3c473ec697f58bdbbf776ac04e5825cce910c0e6a423441a8b56a`  
		Last Modified: Fri, 03 Dec 2021 04:52:20 GMT  
		Size: 62.4 MB (62372158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b342939c972395296f53b6e1c1230c4f0e6596c877cbc0f5c71d7011a032404`  
		Last Modified: Fri, 03 Dec 2021 04:52:30 GMT  
		Size: 105.6 MB (105617251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd32fec3601d43a4fd066550279116adeaad57eef408707f5c3c9674c7fc6dd`  
		Last Modified: Fri, 03 Dec 2021 04:51:53 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
