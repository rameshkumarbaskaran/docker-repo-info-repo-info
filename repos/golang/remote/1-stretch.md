## `golang:1-stretch`

```console
$ docker pull golang@sha256:5e1bdad3f8fbe3cc6eafc8bdcdf0c1cd72b569e10b3ff366f4cfbef8adc4d82d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `golang:1-stretch` - linux; amd64

```console
$ docker pull golang@sha256:024b0d59bf05d622765d8a9b378f79f238a20ef67e66421a721128507255d0a9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.6 MB (303554636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f1969533fd01efc368aeec6cb1b19f88ff29faba5684601873a63828a0ee4d1`
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
# Fri, 04 Mar 2022 01:04:45 GMT
ENV GOLANG_VERSION=1.17.8
# Fri, 04 Mar 2022 01:05:26 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.8.linux-amd64.tar.gz'; 			sha256='980e65a863377e69fd9b67df9d8395fd8e93858e7a24c9f55803421e453f4f99'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.8.linux-armv6l.tar.gz'; 			sha256='3287ca2fe6819fa87af95182d5942bf4fa565aff8f145812c6c70c0466ce25ae'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.8.linux-arm64.tar.gz'; 			sha256='57a9171682e297df1a5bd287be056ed0280195ad079af90af16dcad4f64710cb'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.8.linux-386.tar.gz'; 			sha256='a826cd599828aeefc86d742e1a8ce8ab7e0251b2429568ad5633e21c8a769053'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.8.linux-ppc64le.tar.gz'; 			sha256='2077dd2fc57a74b0630b0c239ae4e3114607311778effd43fcfe5174133ee188'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.8.linux-s390x.tar.gz'; 			sha256='3fac23801644a2f93a1643acecd5a94a5ea05d88e19467092fb6e64205710f61'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 04 Mar 2022 01:05:27 GMT
ENV GOPATH=/go
# Fri, 04 Mar 2022 01:05:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 01:05:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 04 Mar 2022 01:05:28 GMT
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
	-	`sha256:f7a37355856122e3ffc770003babe252d7be045dcb5b6874a11852e7172a67b5`  
		Last Modified: Fri, 04 Mar 2022 01:20:58 GMT  
		Size: 134.9 MB (134903240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16b2ff929d3d32cad888f3973247fb5c02ddd68eca831963be6a41a71558d363`  
		Last Modified: Fri, 04 Mar 2022 01:20:40 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-stretch` - linux; arm variant v7

```console
$ docker pull golang@sha256:817d8f83b153b1df313d397b5afaefe4a57fb8b6644655282ce9cd9b1f9b57d0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.5 MB (251453668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34aaa1e99ed45b287118162c8d87dc7915664df4cd9d7d0f249e25b6ad31bed5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Mar 2022 02:08:52 GMT
ADD file:32b09ecc1f1473cc68b2fe74354febc64a9530d26aa83549020fed06caa8ba8b in / 
# Tue, 01 Mar 2022 02:08:53 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 09:37:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 09:37:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 01 Mar 2022 09:38:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 22:02:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 22:02:07 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 00:50:43 GMT
ENV GOLANG_VERSION=1.17.8
# Fri, 04 Mar 2022 00:51:35 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.8.linux-amd64.tar.gz'; 			sha256='980e65a863377e69fd9b67df9d8395fd8e93858e7a24c9f55803421e453f4f99'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.8.linux-armv6l.tar.gz'; 			sha256='3287ca2fe6819fa87af95182d5942bf4fa565aff8f145812c6c70c0466ce25ae'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.8.linux-arm64.tar.gz'; 			sha256='57a9171682e297df1a5bd287be056ed0280195ad079af90af16dcad4f64710cb'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.8.linux-386.tar.gz'; 			sha256='a826cd599828aeefc86d742e1a8ce8ab7e0251b2429568ad5633e21c8a769053'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.8.linux-ppc64le.tar.gz'; 			sha256='2077dd2fc57a74b0630b0c239ae4e3114607311778effd43fcfe5174133ee188'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.8.linux-s390x.tar.gz'; 			sha256='3fac23801644a2f93a1643acecd5a94a5ea05d88e19467092fb6e64205710f61'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 04 Mar 2022 00:51:37 GMT
ENV GOPATH=/go
# Fri, 04 Mar 2022 00:51:37 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 00:51:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 04 Mar 2022 00:51:39 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:57f32f9fdf459a27691c3a29131c270edd06bf53c003de1f42bb0a6ff8824e31`  
		Last Modified: Tue, 01 Mar 2022 02:25:39 GMT  
		Size: 42.1 MB (42116971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e724a8423f66e29c28d1f7eb411c0fc8b5e925a2dba9d9984b26ba548383e5`  
		Last Modified: Tue, 01 Mar 2022 09:59:33 GMT  
		Size: 10.0 MB (9956523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcdac683edae6f35034917112b5fe629e9a55d8911f2afdd7746b8dfba6c1638`  
		Last Modified: Tue, 01 Mar 2022 09:59:30 GMT  
		Size: 3.9 MB (3921197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3159be5381536c8d0bda312974531e6cb3f82099028dc433bb1d7c20c0cd05e`  
		Last Modified: Tue, 01 Mar 2022 10:00:17 GMT  
		Size: 46.1 MB (46127771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02d823f3f2c8586dc7011f5d67a9cfe154bcb7fabb119cd80dd71416e90cc37`  
		Last Modified: Wed, 02 Mar 2022 22:28:16 GMT  
		Size: 46.2 MB (46193666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c913b48159392c9fe9c9ec44bdcf5dbed905236d6aa41b186296aabf0391228a`  
		Last Modified: Fri, 04 Mar 2022 01:17:52 GMT  
		Size: 103.1 MB (103137383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a56b1199948e28e6e390c752d0aa936ca62242bf4d15825a01ab7ba63c1331b`  
		Last Modified: Fri, 04 Mar 2022 01:16:44 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-stretch` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:bf4bc7d15577a3c9620fe9408234025abec8ff56ce200b341e3492a2430728a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.7 MB (256715580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e8abec6228b13605e8353cac7a8146d1d8cb1b1c67b09370e07b41f5b485815`
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
# Fri, 04 Mar 2022 02:29:17 GMT
ENV GOLANG_VERSION=1.17.8
# Fri, 04 Mar 2022 02:29:32 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.8.linux-amd64.tar.gz'; 			sha256='980e65a863377e69fd9b67df9d8395fd8e93858e7a24c9f55803421e453f4f99'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.8.linux-armv6l.tar.gz'; 			sha256='3287ca2fe6819fa87af95182d5942bf4fa565aff8f145812c6c70c0466ce25ae'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.8.linux-arm64.tar.gz'; 			sha256='57a9171682e297df1a5bd287be056ed0280195ad079af90af16dcad4f64710cb'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.8.linux-386.tar.gz'; 			sha256='a826cd599828aeefc86d742e1a8ce8ab7e0251b2429568ad5633e21c8a769053'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.8.linux-ppc64le.tar.gz'; 			sha256='2077dd2fc57a74b0630b0c239ae4e3114607311778effd43fcfe5174133ee188'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.8.linux-s390x.tar.gz'; 			sha256='3fac23801644a2f93a1643acecd5a94a5ea05d88e19467092fb6e64205710f61'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Fri, 04 Mar 2022 02:29:33 GMT
ENV GOPATH=/go
# Fri, 04 Mar 2022 02:29:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Mar 2022 02:29:36 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 04 Mar 2022 02:29:37 GMT
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
	-	`sha256:a4f4211b541262d8990c5470e2d81fd37f88ff7c44959ee654f3864132b338d1`  
		Last Modified: Fri, 04 Mar 2022 02:41:21 GMT  
		Size: 102.7 MB (102693444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:618b966bc4893071910daba27b7e5aecbdea0f43647f2419e9f52349d33e6707`  
		Last Modified: Fri, 04 Mar 2022 02:41:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-stretch` - linux; 386

```console
$ docker pull golang@sha256:aef6869d1aaf40af7b340f61fbb3ae63bd3f4348361c03f802fbcc37a1c843a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.4 MB (281355077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7867467000e1b31c91be96494c8acbf876e8ac58ce5caa73fdf5df114484705`
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
# Thu, 03 Mar 2022 22:41:26 GMT
ENV GOLANG_VERSION=1.17.8
# Thu, 03 Mar 2022 22:42:08 GMT
RUN set -eux; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	url=; 	case "$arch" in 		'amd64') 			url='https://dl.google.com/go/go1.17.8.linux-amd64.tar.gz'; 			sha256='980e65a863377e69fd9b67df9d8395fd8e93858e7a24c9f55803421e453f4f99'; 			;; 		'armel') 			export GOARCH='arm' GOARM='5' GOOS='linux'; 			;; 		'armhf') 			url='https://dl.google.com/go/go1.17.8.linux-armv6l.tar.gz'; 			sha256='3287ca2fe6819fa87af95182d5942bf4fa565aff8f145812c6c70c0466ce25ae'; 			;; 		'arm64') 			url='https://dl.google.com/go/go1.17.8.linux-arm64.tar.gz'; 			sha256='57a9171682e297df1a5bd287be056ed0280195ad079af90af16dcad4f64710cb'; 			;; 		'i386') 			url='https://dl.google.com/go/go1.17.8.linux-386.tar.gz'; 			sha256='a826cd599828aeefc86d742e1a8ce8ab7e0251b2429568ad5633e21c8a769053'; 			;; 		'mips64el') 			export GOARCH='mips64le' GOOS='linux'; 			;; 		'ppc64el') 			url='https://dl.google.com/go/go1.17.8.linux-ppc64le.tar.gz'; 			sha256='2077dd2fc57a74b0630b0c239ae4e3114607311778effd43fcfe5174133ee188'; 			;; 		's390x') 			url='https://dl.google.com/go/go1.17.8.linux-s390x.tar.gz'; 			sha256='3fac23801644a2f93a1643acecd5a94a5ea05d88e19467092fb6e64205710f61'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 		echo >&2; 		echo >&2 "warning: current architecture ($arch) does not have a compatible Go binary release; will be building from source"; 		echo >&2; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url" --progress=dot:giga; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 		apt-get install -y --no-install-recommends golang-go; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apt-mark auto '.*' > /dev/null; 		apt-mark manual $savedAptMark > /dev/null; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		rm -rf /var/lib/apt/lists/*; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		go version
# Thu, 03 Mar 2022 22:42:09 GMT
ENV GOPATH=/go
# Thu, 03 Mar 2022 22:42:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Mar 2022 22:42:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 03 Mar 2022 22:42:10 GMT
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
	-	`sha256:93d4a0dd5454377c6128768ddc1be62f8df95897f86286c403544a1ad929bd2a`  
		Last Modified: Thu, 03 Mar 2022 23:01:23 GMT  
		Size: 105.7 MB (105678879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd2bdd39a43385d7e4c848b075f0cc1cf7339eb533706df924e6db19f9e08533`  
		Last Modified: Thu, 03 Mar 2022 23:01:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
