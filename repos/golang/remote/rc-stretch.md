## `golang:rc-stretch`

```console
$ docker pull golang@sha256:1cefb08ad0c963f5df34cfcbd886268ab434f066e47f8fc02316a7b9a7716bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `golang:rc-stretch` - linux; amd64

```console
$ docker pull golang@sha256:3de27c6d64a1e9f1f6fbd8a3ca251b7745fa7c758272b1fe8490de6b0fccee62
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.3 MB (310288188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e6ad6abef6bff07e1b982287af8e50dd8199e8f52dfd1043376391c9283770c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:15:54 GMT
ADD file:23c8493cef4b2584f2526f870645f80d71b4572c29b49a264cea842d2aa2ee28 in / 
# Tue, 01 Mar 2022 02:15:54 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 06:31:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 06:31:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 06:32:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 17:55:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 17:55:12 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Mar 2022 17:55:12 GMT
ENV GOLANG_VERSION=1.18rc1
# Wed, 02 Mar 2022 17:56:37 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18rc1.linux-amd64.tar.gz'; 			sha256='9ea4e6adee711e06fa95546e1a9629b63de3aaae85fac9dc752fb533f3e5be23'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18rc1.linux-armv6l.tar.gz'; 			sha256='d7a3f97b23b1e1f2e1a3596ff011e78f93aa8bbd991e2065ac34c18993884ea1'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18rc1.linux-arm64.tar.gz'; 			sha256='e4528a113016872a3715cec37a6c6dad36d76d51a50fa19b33b7673e47e6df44'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18rc1.linux-386.tar.gz'; 			sha256='a4bb0097276fa3523f1ce84dc4ee50fab0b3b0f7fbe72833710434889516c51e'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18rc1.linux-ppc64le.tar.gz'; 			sha256='a2944dfc3ee22efe1b940f122ee36cb4bb446e209116e5e8f244e78682ece981'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18rc1.linux-s390x.tar.gz'; 			sha256='e5578b8cbcc90659496f3930c61c6974c039d32d0573a6726c5d8e62f7e42d68'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18rc1.src.tar.gz'; 		sha256='5cec7a6653008fa85f8821b33665de37be289b7a02f17f36f705a88c43980bb8'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 02 Mar 2022 17:56:40 GMT
ENV GOPATH=/go
# Wed, 02 Mar 2022 17:56:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Mar 2022 17:56:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 02 Mar 2022 17:56:40 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ec52bb9d0b765b0726e476d07a8d9b2f808cf7b380f27c1544afa286fe5578cf`  
		Last Modified: Tue, 01 Mar 2022 02:22:47 GMT  
		Size: 45.4 MB (45381330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f289049e62eb62ae7bd7a8f612cd5b42f36d423951256750f08baa96922b8587`  
		Last Modified: Tue, 01 Mar 2022 06:40:06 GMT  
		Size: 11.3 MB (11301983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e926c3d7ccab64c93f5552646ea61693989e06e27abf8cfdcbd0aad8e78c71d`  
		Last Modified: Tue, 01 Mar 2022 06:40:05 GMT  
		Size: 4.3 MB (4342352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd63791ebe323af1573a61d3e6c93bcf5c12da3b8603289c2b9e8825b045bd3a`  
		Last Modified: Tue, 01 Mar 2022 06:40:25 GMT  
		Size: 49.8 MB (49762476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc1809a7c00d90f801c41b3123445ab523d34b23206062b57a1650338a1abda1`  
		Last Modified: Wed, 02 Mar 2022 18:07:26 GMT  
		Size: 57.9 MB (57863099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211c37d67d60b970c1efc687dfcef0e4f47bba8820cb2f806e8d318d8c2bc0e9`  
		Last Modified: Wed, 02 Mar 2022 18:07:37 GMT  
		Size: 141.6 MB (141636792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf893e5a093733459800c544b74a07a8bae6cd7bd54d92c6aed501579f5f3000`  
		Last Modified: Wed, 02 Mar 2022 18:07:15 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-stretch` - linux; arm variant v7

```console
$ docker pull golang@sha256:e649ea7855942f1f73521bc6ccdb426492caf49dd2e99ad7e6bcdd76704d5fb7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.3 MB (258290274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b3ff0a484b98bc7619e96cb6482f819a4ff36521fc57fca8580d8c80600e0b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Jan 2022 01:47:34 GMT
ADD file:2d0ec7b989e0ef6e7c2d7cdfa1710507ce32d2218c0769aa5adc804e485973dd in / 
# Wed, 26 Jan 2022 01:47:35 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 16:49:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 16:49:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Jan 2022 16:50:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 20:33:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 20:33:41 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Feb 2022 04:22:58 GMT
ENV GOLANG_VERSION=1.18rc1
# Fri, 18 Feb 2022 04:23:51 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18rc1.linux-amd64.tar.gz'; 			sha256='9ea4e6adee711e06fa95546e1a9629b63de3aaae85fac9dc752fb533f3e5be23'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18rc1.linux-armv6l.tar.gz'; 			sha256='d7a3f97b23b1e1f2e1a3596ff011e78f93aa8bbd991e2065ac34c18993884ea1'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18rc1.linux-arm64.tar.gz'; 			sha256='e4528a113016872a3715cec37a6c6dad36d76d51a50fa19b33b7673e47e6df44'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18rc1.linux-386.tar.gz'; 			sha256='a4bb0097276fa3523f1ce84dc4ee50fab0b3b0f7fbe72833710434889516c51e'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18rc1.linux-ppc64le.tar.gz'; 			sha256='a2944dfc3ee22efe1b940f122ee36cb4bb446e209116e5e8f244e78682ece981'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18rc1.linux-s390x.tar.gz'; 			sha256='e5578b8cbcc90659496f3930c61c6974c039d32d0573a6726c5d8e62f7e42d68'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18rc1.src.tar.gz'; 		sha256='5cec7a6653008fa85f8821b33665de37be289b7a02f17f36f705a88c43980bb8'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 18 Feb 2022 04:23:53 GMT
ENV GOPATH=/go
# Fri, 18 Feb 2022 04:23:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Feb 2022 04:23:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 18 Feb 2022 04:23:56 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a4becb4205b812ec841e47cdf4840f3cd4afedb320617c1a611bd7daacd1b1e2`  
		Last Modified: Wed, 26 Jan 2022 02:05:16 GMT  
		Size: 42.1 MB (42116772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19142ccd43f320261157cec769910c598094bd2f6235ca3fb72f11ff969ba877`  
		Last Modified: Wed, 26 Jan 2022 17:12:46 GMT  
		Size: 10.0 MB (9956581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26bc45f0a06bfebcf8cb3dd7f3b1577bb99c1c9a19b3dc44bab307cdd59267bb`  
		Last Modified: Wed, 26 Jan 2022 17:12:42 GMT  
		Size: 3.9 MB (3921220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f5aa09ea754ba47aefee810b542e69d5f77d134463813ea07489fa9ec46932`  
		Last Modified: Wed, 26 Jan 2022 17:13:26 GMT  
		Size: 46.1 MB (46126065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcebddff60b038c4a2d28edf63a333bffa990ce9a3f4fb80a0ed3c69a94d29d3`  
		Last Modified: Thu, 27 Jan 2022 20:51:05 GMT  
		Size: 46.2 MB (46193612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ab7680f0daaeb8bc93086e31f1af686d03e9a34e1a61a861aaa19d3dbb11b6`  
		Last Modified: Fri, 18 Feb 2022 05:02:35 GMT  
		Size: 110.0 MB (109975868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9538d822db33ec3b7f151a2fef121ad25b8a0d26fe6178fa2154e2270ed8ded1`  
		Last Modified: Fri, 18 Feb 2022 05:01:24 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-stretch` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:70072a2783cb41cf0c6ef2f757234d8b24eb02ee5ef0f66931b7119aae49435b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.6 MB (262644699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f7e6422626dbacd4c4b60347264ecce0963ee05cfa9c0d8350a52678cabdc45`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:47 GMT
ADD file:2b622f607981bbf2484685f44a5147c3bf81f757fd9129e77f97f72fecc0a0db in / 
# Tue, 01 Mar 2022 02:13:48 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:38:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:38:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 10:39:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 06:59:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 06:59:17 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Mar 2022 06:59:18 GMT
ENV GOLANG_VERSION=1.18rc1
# Wed, 02 Mar 2022 07:00:18 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18rc1.linux-amd64.tar.gz'; 			sha256='9ea4e6adee711e06fa95546e1a9629b63de3aaae85fac9dc752fb533f3e5be23'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18rc1.linux-armv6l.tar.gz'; 			sha256='d7a3f97b23b1e1f2e1a3596ff011e78f93aa8bbd991e2065ac34c18993884ea1'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18rc1.linux-arm64.tar.gz'; 			sha256='e4528a113016872a3715cec37a6c6dad36d76d51a50fa19b33b7673e47e6df44'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18rc1.linux-386.tar.gz'; 			sha256='a4bb0097276fa3523f1ce84dc4ee50fab0b3b0f7fbe72833710434889516c51e'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18rc1.linux-ppc64le.tar.gz'; 			sha256='a2944dfc3ee22efe1b940f122ee36cb4bb446e209116e5e8f244e78682ece981'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18rc1.linux-s390x.tar.gz'; 			sha256='e5578b8cbcc90659496f3930c61c6974c039d32d0573a6726c5d8e62f7e42d68'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18rc1.src.tar.gz'; 		sha256='5cec7a6653008fa85f8821b33665de37be289b7a02f17f36f705a88c43980bb8'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 02 Mar 2022 07:00:19 GMT
ENV GOPATH=/go
# Wed, 02 Mar 2022 07:00:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Mar 2022 07:00:22 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 02 Mar 2022 07:00:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4b9bff972ef4bcbae575403d0d7d36292022bd8d6466c8d00eca1a07d53bb6b2`  
		Last Modified: Tue, 01 Mar 2022 02:22:12 GMT  
		Size: 43.2 MB (43173741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f7e36b820d8a64c7408043d6ba8ddedc0dba4cbda7c78cfd0a29be219bf807`  
		Last Modified: Tue, 01 Mar 2022 10:47:56 GMT  
		Size: 10.2 MB (10217036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46857bc495b245fc1d6a1490f0d99dc837a5b9691d98957547996ef83b5f971`  
		Last Modified: Tue, 01 Mar 2022 10:47:55 GMT  
		Size: 3.9 MB (3873880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805e06b03375b28c4382bb8d0195b7219f73c21d15504b22b1d9df8d1336b7c9`  
		Last Modified: Tue, 01 Mar 2022 10:48:14 GMT  
		Size: 47.7 MB (47734377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3dc0a51e88ad1ffbaa140868ab4a240c62badfa6b95d7d720b95d20b3f92495`  
		Last Modified: Wed, 02 Mar 2022 07:12:07 GMT  
		Size: 49.0 MB (49022976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424f1c3aaa605c5d43a33b3cdbf84b11679433d8585055d44c9534ebf8f9aa45`  
		Last Modified: Wed, 02 Mar 2022 07:12:16 GMT  
		Size: 108.6 MB (108622563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91a5178aaa445dd2acae8428bf795167659550a458010953196bfd40852c6c1`  
		Last Modified: Wed, 02 Mar 2022 07:11:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:rc-stretch` - linux; 386

```console
$ docker pull golang@sha256:155db499efc79d6de41286426f529ae49adf93be21dd916c794cce0440382edc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.5 MB (288468873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:515382c3a268a0b5a970f2cc43b7766aaa788ccd1a6721fccbdf9ff5361c3832`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:10:13 GMT
ADD file:bc15f0e456e3757963e61c9b01f81ce157b35fb751d837cf7b6ddd9277872821 in / 
# Tue, 01 Mar 2022 02:10:13 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 05:46:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 05:46:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 05:46:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 04:41:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 04:41:31 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Mar 2022 04:41:32 GMT
ENV GOLANG_VERSION=1.18rc1
# Wed, 02 Mar 2022 04:43:00 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.18rc1.linux-amd64.tar.gz'; 			sha256='9ea4e6adee711e06fa95546e1a9629b63de3aaae85fac9dc752fb533f3e5be23'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.18rc1.linux-armv6l.tar.gz'; 			sha256='d7a3f97b23b1e1f2e1a3596ff011e78f93aa8bbd991e2065ac34c18993884ea1'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.18rc1.linux-arm64.tar.gz'; 			sha256='e4528a113016872a3715cec37a6c6dad36d76d51a50fa19b33b7673e47e6df44'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.18rc1.linux-386.tar.gz'; 			sha256='a4bb0097276fa3523f1ce84dc4ee50fab0b3b0f7fbe72833710434889516c51e'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.18rc1.linux-ppc64le.tar.gz'; 			sha256='a2944dfc3ee22efe1b940f122ee36cb4bb446e209116e5e8f244e78682ece981'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.18rc1.linux-s390x.tar.gz'; 			sha256='e5578b8cbcc90659496f3930c61c6974c039d32d0573a6726c5d8e62f7e42d68'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.18rc1.src.tar.gz'; 		sha256='5cec7a6653008fa85f8821b33665de37be289b7a02f17f36f705a88c43980bb8'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Wed, 02 Mar 2022 04:43:01 GMT
ENV GOPATH=/go
# Wed, 02 Mar 2022 04:43:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Mar 2022 04:43:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 02 Mar 2022 04:43:02 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4d460050f4b628f05281226d933aa11a10afffc452771e0d9dd815bb6858e254`  
		Last Modified: Tue, 01 Mar 2022 02:20:11 GMT  
		Size: 46.1 MB (46097796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f57a4965e785e81bf52d7df87a7b3b5abeeb384075fef0b195b12bdf3864206`  
		Last Modified: Tue, 01 Mar 2022 05:56:48 GMT  
		Size: 11.4 MB (11359682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc782b42f9af37d9d74bb076c8d6bb03945730f16d04982ff3a85814c557f12e`  
		Last Modified: Tue, 01 Mar 2022 05:56:47 GMT  
		Size: 4.6 MB (4564923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d56af1c75591c3524a488450e5adc45a5754e8c91dbfe711564884f78bbc6c`  
		Last Modified: Tue, 01 Mar 2022 05:57:12 GMT  
		Size: 51.3 MB (51265739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22bd6bb39146e30d3f0db39ba80a8a3f3fc6595091b8d64dc68e02e39fd17c1d`  
		Last Modified: Wed, 02 Mar 2022 04:56:49 GMT  
		Size: 62.4 MB (62387903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b97c17f1f243ed714baa159bba4c53a72f0c7d2afa51ae499a0efd908ee2d539`  
		Last Modified: Wed, 02 Mar 2022 04:57:04 GMT  
		Size: 112.8 MB (112792676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c52301db1101fea396174bbe01be911a0d87134fd0ae1883e01476b6cc1ca95`  
		Last Modified: Wed, 02 Mar 2022 04:56:06 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
