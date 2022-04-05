## `caddy:2-builder-alpine`

```console
$ docker pull caddy@sha256:9683635eba95d8ac3eeeb7ad51a3946b3d7922e05ae1f010b41ff20466431e35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:2-builder-alpine` - linux; amd64

```console
$ docker pull caddy@sha256:80234a9cd66af5a747785958e8dc683a43dfe946b9b98c9ffe2806fa4ac5422e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121342541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa54d86d06fba28c500cfe838c151623b997c5e35b2af29ea8b70b6a92a7fb8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 05:32:39 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 05:32:40 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 05:32:40 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 05:37:30 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 05:39:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 05:39:29 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 05:39:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 05:39:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 05:39:30 GMT
WORKDIR /go
# Tue, 05 Apr 2022 15:45:54 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 05 Apr 2022 15:45:54 GMT
ENV XCADDY_VERSION=v0.2.1
# Tue, 05 Apr 2022 15:45:54 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 15:45:54 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Apr 2022 15:45:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Apr 2022 15:45:55 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Apr 2022 15:45:55 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52dc419b0ee22d1bb5f3b95a57b2edc733b7b585277f8101db7b2c9b53605c1b`  
		Last Modified: Tue, 05 Apr 2022 05:42:31 GMT  
		Size: 272.0 KB (271965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bc292e5bacdd8b97a1632a82d0fd0ee6c2692409bd4b35cb9e7e652efbc7c8`  
		Last Modified: Tue, 05 Apr 2022 05:42:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dea7a3ad9148616176ac7fd686181a6e3c4eaac3746166e678a11017e4d32d9`  
		Last Modified: Tue, 05 Apr 2022 05:43:55 GMT  
		Size: 110.2 MB (110188123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35228ee6d672a4ef2501b746851ae8dc63cdc2612057a726a7affcd9d7d9f08`  
		Last Modified: Tue, 05 Apr 2022 05:43:41 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431098d05c7f64b1b215f6e58d58584efa1b85c22de1e46eabdf9f41c9a31550`  
		Last Modified: Tue, 05 Apr 2022 15:46:24 GMT  
		Size: 6.8 MB (6821467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16611ed52579f2526e4c8ef7d32963cc52bdf84706c195aaea01082575369d8d`  
		Last Modified: Tue, 05 Apr 2022 15:46:23 GMT  
		Size: 1.2 MB (1245713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f56bc9474ab53335737725ec3c82362fd8d085309b54710629fec01fac471c3d`  
		Last Modified: Tue, 05 Apr 2022 15:46:22 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:3b65e4ace88f181e88d38888c2e7bf45ab2ea95d2a70d1aa9e260a7e37265b78
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115819432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f23978f531de3d6637fd8f52ffd68708d73a8f566c332f38f8098827478041`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 29 Mar 2022 00:49:32 GMT
ADD file:44acf536d487bec7f7bf16561f4ec90e60d4447b3cbabfeca66953c4491aabeb in / 
# Tue, 29 Mar 2022 00:49:33 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 07:40:30 GMT
RUN apk add --no-cache ca-certificates
# Tue, 29 Mar 2022 07:40:32 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 07:40:32 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 07:48:57 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 29 Mar 2022 07:52:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 29 Mar 2022 07:52:15 GMT
ENV GOPATH=/go
# Tue, 29 Mar 2022 07:52:16 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 07:52:17 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 29 Mar 2022 07:52:18 GMT
WORKDIR /go
# Tue, 29 Mar 2022 19:48:04 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 29 Mar 2022 19:48:04 GMT
ENV XCADDY_VERSION=v0.2.1
# Tue, 29 Mar 2022 19:48:05 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 29 Mar 2022 19:48:05 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 29 Mar 2022 19:48:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 29 Mar 2022 19:48:08 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 29 Mar 2022 19:48:09 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:84f033dabe5013c0dfae4263abd951011719d0a15adc3c7312c5be994deff030`  
		Last Modified: Tue, 29 Mar 2022 00:51:25 GMT  
		Size: 2.6 MB (2621943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026b5f27b2698e668042c86dd2538d12d411867d83d2a9d9af230e055fe5a181`  
		Last Modified: Tue, 29 Mar 2022 07:57:23 GMT  
		Size: 272.1 KB (272137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0516ac9f12d388332faafff86659644eed1224227ceb75f6ce803e022d535e`  
		Last Modified: Tue, 29 Mar 2022 07:57:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a782b491ecfba149c412f8ad872bcfa7287e6a7caa6357cdcfbcb807c8da98f0`  
		Last Modified: Tue, 29 Mar 2022 08:01:44 GMT  
		Size: 105.1 MB (105068727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c866997cbd03bebd88e007f49e1a9487fd4ba581dfa2a4d85eff8629736d28`  
		Last Modified: Tue, 29 Mar 2022 08:00:34 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0607471521c979ff3df274d2a499d8cdb7828e08615e4a430c0732444a298c53`  
		Last Modified: Tue, 29 Mar 2022 19:49:56 GMT  
		Size: 6.7 MB (6677400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38cc531d7dbc490a2d6e6a7000ff2d423828e739ab7213320c86a635cdfc3005`  
		Last Modified: Tue, 29 Mar 2022 19:49:54 GMT  
		Size: 1.2 MB (1178510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceed9226afbdee75100b0fe36dc64b2212a63594d9d0cd2c83756c32f4cc37b2`  
		Last Modified: Tue, 29 Mar 2022 19:49:54 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:f54ac7197b1808cf8669ba548743d7451145fde7f106a625719734ccc91c22e3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114678401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8964981be06d6508dae7667bbb24f7e3fd14fd6c3cb3fd7c4c98920d38c243d1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 29 Mar 2022 02:13:28 GMT
ADD file:8c959b80e3661beea7b3468017b88897d981bf52ed43c074e7c87ecb753e9059 in / 
# Tue, 29 Mar 2022 02:13:28 GMT
CMD ["/bin/sh"]
# Wed, 30 Mar 2022 05:12:01 GMT
RUN apk add --no-cache ca-certificates
# Wed, 30 Mar 2022 05:12:02 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 30 Mar 2022 05:12:03 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 05:20:26 GMT
ENV GOLANG_VERSION=1.17.8
# Wed, 30 Mar 2022 05:23:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Wed, 30 Mar 2022 05:23:37 GMT
ENV GOPATH=/go
# Wed, 30 Mar 2022 05:23:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 05:23:39 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Wed, 30 Mar 2022 05:23:39 GMT
WORKDIR /go
# Thu, 31 Mar 2022 10:16:41 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 31 Mar 2022 10:16:41 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 31 Mar 2022 10:16:41 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 31 Mar 2022 10:16:42 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 31 Mar 2022 10:16:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 31 Mar 2022 10:16:45 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 31 Mar 2022 10:16:45 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:22b1e5a07a97d7af6fdc335e3b3a975b73908fa19b084289c408a00814da0398`  
		Last Modified: Tue, 29 Mar 2022 02:15:28 GMT  
		Size: 2.4 MB (2424303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18afe8b0e9a71d00d5b941e9e0041cc6e1f1ae69c57e1afff55db8d7a607f29`  
		Last Modified: Wed, 30 Mar 2022 05:30:21 GMT  
		Size: 271.1 KB (271113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08ddb804f8aeaec8eff8311748df0f04749eddb4913d678fab8ab20a3b46f580`  
		Last Modified: Wed, 30 Mar 2022 05:30:21 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4edf12630c16257662f2bdf20d90a5bf45d8e96352e57b2b0683a2c992633661`  
		Last Modified: Wed, 30 Mar 2022 05:34:59 GMT  
		Size: 104.9 MB (104853402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fda448bbd5f8b13a3177b8d936c9ebf36c5b6b6afb115032b335ffbabcc86a3`  
		Last Modified: Wed, 30 Mar 2022 05:33:50 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af794078fed87f645391e880bc1d665d1524e29f1e6e48e61baed0eb0e8e6793`  
		Last Modified: Thu, 31 Mar 2022 10:18:34 GMT  
		Size: 6.0 MB (5952157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c161e9c95bfb3912bc4c31b22c3926ec814b500b7c1a29440b70e246e9f4c393`  
		Last Modified: Thu, 31 Mar 2022 10:18:32 GMT  
		Size: 1.2 MB (1176712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19426f19dc9f476978016fa31a79dce87b8a57b58c8129d63cf484e57abcccec`  
		Last Modified: Thu, 31 Mar 2022 10:18:32 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:bd154e37f9c5a0404d81e98df605e6c98851420eae03898c2cb4ef59d74de4e9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115488239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22be460f532c232d1f8456b6f51aff00852870f3c1dcf3116bc74e44f2092eab`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:05 GMT
ADD file:24e8b04304ef91bbf949674909ccaf2c66e3dcd096c3c307a0510569eadf576f in / 
# Tue, 29 Mar 2022 00:40:05 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 10:21:12 GMT
RUN apk add --no-cache ca-certificates
# Tue, 29 Mar 2022 10:21:13 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 10:21:14 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 10:25:50 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 29 Mar 2022 10:27:29 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 29 Mar 2022 10:27:29 GMT
ENV GOPATH=/go
# Tue, 29 Mar 2022 10:27:30 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 10:27:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 29 Mar 2022 10:27:32 GMT
WORKDIR /go
# Wed, 30 Mar 2022 19:20:28 GMT
RUN apk add --no-cache     git     ca-certificates
# Wed, 30 Mar 2022 19:20:28 GMT
ENV XCADDY_VERSION=v0.2.1
# Wed, 30 Mar 2022 19:20:29 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 30 Mar 2022 19:20:30 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 30 Mar 2022 19:20:32 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Wed, 30 Mar 2022 19:20:34 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Wed, 30 Mar 2022 19:20:34 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:80fa7f07ec7b717ec5f8e2717b91e3d659e129052ec3def2570a5674322688d9`  
		Last Modified: Tue, 29 Mar 2022 00:41:08 GMT  
		Size: 2.7 MB (2716347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c6364a84307e93e20f5cfdbcb427b0daaa069d79542d73803f5f27a713d499`  
		Last Modified: Tue, 29 Mar 2022 10:31:05 GMT  
		Size: 271.8 KB (271770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3ee05828bc6499750a0be2b46f395a3d70512909fa3247f7482bca1d4fcaf3`  
		Last Modified: Tue, 29 Mar 2022 10:31:05 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56812c1e0db941b796796a0d23cc13e567c7f50251e6bdfcfa2f5f7ce1f025c1`  
		Last Modified: Tue, 29 Mar 2022 10:32:41 GMT  
		Size: 104.4 MB (104424776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6676495bf358590a4b13d87316a6e3db7be759723dfeb83d0e4654781bcca7f9`  
		Last Modified: Tue, 29 Mar 2022 10:32:25 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b3c2b3c2b73653ff0e345014516d5022405856ad941f346ecd1efe5139c817d`  
		Last Modified: Wed, 30 Mar 2022 19:21:27 GMT  
		Size: 6.9 MB (6925983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1325856e660832c566905079f4b2a511f6cebb65e1ab2cf5948e8ee8c195d70`  
		Last Modified: Wed, 30 Mar 2022 19:21:26 GMT  
		Size: 1.1 MB (1148677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ed4958be165477af667a4cc883321e4dfa792d1721bbd3354de465573b4ea7`  
		Last Modified: Wed, 30 Mar 2022 19:21:26 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:62551ee42f52d91896772682bf9afd720e7e61787c803c88bccdc0a0f610e8fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.3 MB (114312321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6409a922bde06452fefb86d337c15572d5016ffe5ab9479118c0271838f40d6b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 29 Mar 2022 00:16:52 GMT
ADD file:9e7b65a431d59070abaadae56d9c3fc59c899af881939e4353b1f524b2bd5185 in / 
# Tue, 29 Mar 2022 00:16:55 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 07:15:11 GMT
RUN apk add --no-cache ca-certificates
# Tue, 29 Mar 2022 07:15:18 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 29 Mar 2022 07:15:22 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 07:23:06 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 29 Mar 2022 07:25:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 29 Mar 2022 07:25:47 GMT
ENV GOPATH=/go
# Tue, 29 Mar 2022 07:25:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 07:25:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 29 Mar 2022 07:26:00 GMT
WORKDIR /go
# Thu, 31 Mar 2022 01:26:44 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 31 Mar 2022 01:26:47 GMT
ENV XCADDY_VERSION=v0.2.1
# Thu, 31 Mar 2022 01:26:50 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 31 Mar 2022 01:26:52 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 31 Mar 2022 01:27:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 31 Mar 2022 01:27:04 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 31 Mar 2022 01:27:07 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:1c611bca4fa49cac5bc1e3826ad53fee85ed659d24bffcccd86c3f04be07339a`  
		Last Modified: Tue, 29 Mar 2022 00:18:26 GMT  
		Size: 2.8 MB (2811009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385dfa020282a03d5b95fb5db383e66beca36ce2f20ff89f035066e2dda0b62a`  
		Last Modified: Tue, 29 Mar 2022 07:30:25 GMT  
		Size: 274.2 KB (274166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c989adaca2aebf8ea15071191301f7df3cda1d8f56ef74c0dcbd982f482284`  
		Last Modified: Tue, 29 Mar 2022 07:30:25 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce98db651e1892c2f3054cb692a00e350eedbb6ec446a7ad44c40a2b56db8879`  
		Last Modified: Tue, 29 Mar 2022 07:32:20 GMT  
		Size: 102.8 MB (102784611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb3362f657d5563c2e69ca0c3e1d1f0fc1f5c93196f924107e12388b726cb16`  
		Last Modified: Tue, 29 Mar 2022 07:32:03 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efccddc9b8491114a0fdc8352ed68d335c28898059b6e54b32b825e4e699cb3`  
		Last Modified: Thu, 31 Mar 2022 01:28:38 GMT  
		Size: 7.3 MB (7320980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440fd41c20b3196142546c5f0b807f5c413161da363ec1aa8159e03e0016c12f`  
		Last Modified: Thu, 31 Mar 2022 01:28:37 GMT  
		Size: 1.1 MB (1120843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f5f93275ada45861c6a714ca4e04c543a790c2eac1b9de20b831977a3bd986`  
		Last Modified: Thu, 31 Mar 2022 01:28:37 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:7862e378800416206aa5844ed260f8cb64c1537299e481e5004521024727c011
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118747451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d95993f92df472d91942633064b5db1e229654fbf9e15e574f235f732d2171`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 04 Apr 2022 23:41:39 GMT
ADD file:f22e4b2be87d3c59c8c609acf79015938dc1fba0b26d7c1b59bd0fc36d63a906 in / 
# Mon, 04 Apr 2022 23:41:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:08:51 GMT
RUN apk add --no-cache ca-certificates
# Tue, 05 Apr 2022 06:44:34 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 05 Apr 2022 06:44:35 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 06:48:26 GMT
ENV GOLANG_VERSION=1.17.8
# Tue, 05 Apr 2022 06:49:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.17.8.src.tar.gz'; 		sha256='2effcd898140da79a061f3784ca4f8d8b13d811fb2abe9dad2404442dabbdf7a'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Tue, 05 Apr 2022 06:49:56 GMT
ENV GOPATH=/go
# Tue, 05 Apr 2022 06:49:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 06:49:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 05 Apr 2022 06:49:57 GMT
WORKDIR /go
# Tue, 05 Apr 2022 14:02:01 GMT
RUN apk add --no-cache     git     ca-certificates
# Tue, 05 Apr 2022 14:02:02 GMT
ENV XCADDY_VERSION=v0.2.1
# Tue, 05 Apr 2022 14:02:02 GMT
ENV CADDY_VERSION=v2.4.6
# Tue, 05 Apr 2022 14:02:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 05 Apr 2022 14:02:03 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='30621f45934c6450dcf6ca790f2763a334ce58048a50e6d2b552a145da6cc0b79e454724d9953483794119c1b90555a8657e6311940cb37dd21c193e22459252' ;; 		armhf)   binArch='armv6'; checksum='5d1265a07be13aa9f2c9d8ad9a75d5658bca1dfc66c2b1b100b517edf4ac7a1fe18494c7b01b3856102e1cfc912912d049393accd8b1ef22f73bfc22bb27daec' ;; 		armv7)   binArch='armv7'; checksum='04e1b4c14def100db4c2da0c08d2bd48f1e965a6250763659a5e435d2815559483f7ce533e36cca9a15709508deab133972b19ff87a76f15ea01876a62e49edf' ;; 		aarch64) binArch='arm64'; checksum='e4cabca39b61c6a7956b828e9b1e1c39e802b65a1c1e3ce44d93bcffaafce6625884315815051f08209deb53a294101bf9c60ffbf000ac8ce2ba38a13e8e2287' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='ff1cc638ee18ce3ef36097547db9cdc3ff27f8ce46d8df50273663655ccea909a8396a01b4a144d57ad7e896ec6aef052c31f516c2a9c7e08d04a27228cf1c42' ;; 		s390x)   binArch='s390x'; checksum='335a7436927378508e0d55b74898b8d36f73f7a8ceaaa038c0ac054ab79c96b77acb642fb7881a07358b161e6e54efb8db0eacd0bd10f8f151698de517bffa0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.2.1/xcaddy_0.2.1_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 05 Apr 2022 14:02:03 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 05 Apr 2022 14:02:03 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:a27b630f446c3da376a30cf610e4bfa6847f8b87c83702c29e72b986f4e52d28`  
		Last Modified: Mon, 04 Apr 2022 23:42:37 GMT  
		Size: 2.6 MB (2600375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72593bb761a2ce336603e9e84973d1e284f39e0188e758ad8bc22c45cd9b6395`  
		Last Modified: Tue, 05 Apr 2022 06:09:13 GMT  
		Size: 272.3 KB (272267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf480933488ffcb2c9c9269292e2e3d643bea6eeb04cf948790ca50666a61c8`  
		Last Modified: Tue, 05 Apr 2022 06:53:15 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b3e51e0eff0c3e6118a6448425ada0b8e1725d738559d5b5e29ef58c570e8d`  
		Last Modified: Tue, 05 Apr 2022 06:54:30 GMT  
		Size: 107.7 MB (107739421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86765c73189fadce4ca276af5f7d9440213d5986a9687b648a51d45978e3a8c4`  
		Last Modified: Tue, 05 Apr 2022 06:54:17 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f50aeaf488b81d4c5d54c453b47637b6fbdfae9ca014728018463ce30aa78b`  
		Last Modified: Tue, 05 Apr 2022 14:03:02 GMT  
		Size: 6.9 MB (6930892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca74c757745c5b39f811e1b5ed2a0fe0b8f2de2ab52b23dd01d8aaa71540d27b`  
		Last Modified: Tue, 05 Apr 2022 14:03:02 GMT  
		Size: 1.2 MB (1203782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e4f898506aece97cc68bfd9e1a347bd072242e4672eee262eae303b3e0b6e9`  
		Last Modified: Tue, 05 Apr 2022 14:03:02 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
