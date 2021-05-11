## `caddy:2-builder`

```console
$ docker pull caddy@sha256:425b1075398c4ebde59024ee2847746c5b54171ee16096bb85d4a99aa6de8398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `caddy:2-builder` - linux; amd64

```console
$ docker pull caddy@sha256:046f9aa5dcf83fb25e28e43539c520c8cd0dfe05faf14ad780826c7c36775145
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.5 MB (116541075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd288b16c2ac5e35de34025c916a8a52cb8c3c35644e3e2beee860100beea6de`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:27:12 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 21:27:13 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 21:27:13 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:18:07 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 23:20:04 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 	sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 23:20:05 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 23:20:05 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:20:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 23:20:07 GMT
WORKDIR /go
# Fri, 07 May 2021 01:56:14 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 01:56:14 GMT
ENV XCADDY_VERSION=v0.1.9
# Tue, 11 May 2021 01:04:35 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 01:04:36 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 11 May 2021 01:04:37 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 11 May 2021 01:04:38 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 11 May 2021 01:04:38 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcc1eea9eeabb6de296adb3e0c1b0722cf13251ff3e4e2d0a5f7ed8e3d48342`  
		Last Modified: Wed, 14 Apr 2021 21:35:06 GMT  
		Size: 281.3 KB (281269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4ab2625f07be8d5c6e48046a05ff3ecc7f374b794a926fb62247b66b511909`  
		Last Modified: Wed, 14 Apr 2021 21:35:06 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e7595549f7536d76f08a8a23fb67e3e6fae08ccf3add715c5c1c956f9445d2`  
		Last Modified: Thu, 06 May 2021 23:29:42 GMT  
		Size: 105.7 MB (105745828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df88182f7acff97ffde9f614a0fd86e8a26590e445aa76e442c3a79d9e4c4f4`  
		Last Modified: Thu, 06 May 2021 23:29:25 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d573d19fd03835237c7687f4f394fa6b1fc1c894a901f2853846256ee7746eb`  
		Last Modified: Fri, 07 May 2021 01:56:57 GMT  
		Size: 6.4 MB (6390123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95db25f5b69783a08df8902a5330daddf1e8b10bd1d8401b25d8f8ab43b6586f`  
		Last Modified: Tue, 11 May 2021 01:05:15 GMT  
		Size: 1.3 MB (1311169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74bfbae6287f60c1e9b89dd3e92e73d9f949ee6f11d78bc97a3e945ee20b2c68`  
		Last Modified: Tue, 11 May 2021 01:05:14 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:124237c870217e836b67b4697d7cddad2c3c58d50878dc51654db3605712c336
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.3 MB (112278566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15bef88e43f4622abd673fe82f110eb193559dd1abb2d8550178eb66032b4b5f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:00:55 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:01:01 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:01:02 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 21:24:09 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 21:27:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 	sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 21:27:32 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 21:27:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 21:27:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 21:27:35 GMT
WORKDIR /go
# Thu, 06 May 2021 22:10:19 GMT
RUN apk add --no-cache     git     ca-certificates
# Thu, 06 May 2021 22:10:20 GMT
ENV XCADDY_VERSION=v0.1.9
# Mon, 10 May 2021 23:51:04 GMT
ENV CADDY_VERSION=v2.4.0
# Mon, 10 May 2021 23:51:07 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 10 May 2021 23:51:12 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 10 May 2021 23:51:14 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 10 May 2021 23:51:16 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4dea9fd179326b36ea137aad07e06571ffe7ad849e2a13a32354dcfd5d858d`  
		Last Modified: Wed, 14 Apr 2021 21:14:02 GMT  
		Size: 281.4 KB (281379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abeb04d84d23abf8470fc95982483a9117a87e55b13c591f5332a460a5233bb`  
		Last Modified: Wed, 14 Apr 2021 21:14:02 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a3721aaa7ffedbec829a557c2d5f99c4661695a51f82632ece4df509b71bc1`  
		Last Modified: Thu, 06 May 2021 21:38:30 GMT  
		Size: 101.9 MB (101925593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298c78bc6b40a671a2f9a64d2cecf253acd10da30924ff687012e02b0307a1a8`  
		Last Modified: Thu, 06 May 2021 21:37:54 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3d237d41fc2805c9d9a047d4bb2618233c7093cc31d682b5231e0261a8c201`  
		Last Modified: Thu, 06 May 2021 22:11:03 GMT  
		Size: 6.2 MB (6227066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ffbb7f2dd65c638ffd56b2ab5964193545041922501d15451a2b6f4b0b0edb`  
		Last Modified: Mon, 10 May 2021 23:51:50 GMT  
		Size: 1.2 MB (1221678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d30db79a4a633e8984befac9884a645ed6f3bd581f677daa8a26f2cbda65a4`  
		Last Modified: Mon, 10 May 2021 23:51:50 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:a4ecc2040cdcc0166a3fea577c4e704d291fe70c2c65c460ff347d06c2b54046
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 MB (111227459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d2c6dfa3a578099a3e909c80cd793b780fb7a9135d5f28ec25270157a0902f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:00:38 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 21:01:31 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 21:01:41 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:11:51 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 23:15:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 	sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 23:15:25 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 23:15:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:15:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 23:15:29 GMT
WORKDIR /go
# Fri, 07 May 2021 02:34:14 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 02:34:14 GMT
ENV XCADDY_VERSION=v0.1.9
# Tue, 11 May 2021 01:17:54 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 01:18:06 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 11 May 2021 01:18:29 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 11 May 2021 01:18:32 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 11 May 2021 01:18:34 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb6bd423db0b63fdc83c72eae7ef401cb2fb9eaa63961c71a867ff26bfe422f`  
		Last Modified: Wed, 14 Apr 2021 22:44:20 GMT  
		Size: 280.5 KB (280532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835b667ae68ff940439602ffbabae6e923c687cb56c62a793f23ddca67584049`  
		Last Modified: Wed, 14 Apr 2021 22:44:20 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5b93a32354ff48887c2e9c4540875b8aa57822ab5c261d95e3c186d27b5c5e`  
		Last Modified: Thu, 06 May 2021 23:28:23 GMT  
		Size: 101.7 MB (101743890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2925b4cee8520caf8150ba3410d1306c50fa326f2fd920488f9e432578fda5`  
		Last Modified: Thu, 06 May 2021 23:27:52 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc435726a63967cbbe522309fca3524e0e1fd01e955717cedc9e172d632cbd1`  
		Last Modified: Fri, 07 May 2021 02:34:54 GMT  
		Size: 5.6 MB (5558665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd402931cf263713336d2aa524723f4caec26b90c0d6406651b14a2f88a642ab`  
		Last Modified: Tue, 11 May 2021 01:19:24 GMT  
		Size: 1.2 MB (1219508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee3295bff1b446bc98e483336ce527bcd52ccfecd1930eba95c70c26e909f3a`  
		Last Modified: Tue, 11 May 2021 01:19:23 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:a8418ff913feb35632b8e2e0e2dde138632b289047de19713b0c24fe65c6eecc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.8 MB (111763060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68622e818b4c271dd7faf093081a9641f809d407eb6dc67bb6afe822393b4b0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:40:18 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:40:49 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:40:55 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 22:31:41 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 22:33:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 	sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 22:33:53 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 22:33:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 22:33:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 22:33:57 GMT
WORKDIR /go
# Fri, 07 May 2021 01:17:18 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 01:17:19 GMT
ENV XCADDY_VERSION=v0.1.9
# Mon, 10 May 2021 23:40:20 GMT
ENV CADDY_VERSION=v2.4.0
# Mon, 10 May 2021 23:40:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 10 May 2021 23:40:24 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 10 May 2021 23:40:25 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 10 May 2021 23:40:26 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7186ed65a4f7bb0e9cd4b00f43359b47a4f19749dbd48e704fc578a4f43d7c96`  
		Last Modified: Wed, 14 Apr 2021 20:59:32 GMT  
		Size: 281.5 KB (281488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:316046926c0ae5f42710c1197ed3de9fc374986179c18611f523cf4521adeef1`  
		Last Modified: Wed, 14 Apr 2021 20:59:32 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696a969ea94b7c2e3938ec670b72c32f58ece636bb7ec6526d0efab40e760bce`  
		Last Modified: Thu, 06 May 2021 22:44:20 GMT  
		Size: 101.1 MB (101090590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff4d3f41a5567d10cda7e4f3c4267dbb9181eb63bb52c950c3dce3327a9a36e`  
		Last Modified: Thu, 06 May 2021 22:43:56 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ec12dccc6ac2c5238a0e958e58c89d37f56cf2e181ba8a4f291b176a2a20fa`  
		Last Modified: Fri, 07 May 2021 01:18:00 GMT  
		Size: 6.5 MB (6476691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803dba8659a2ec5c5a177383797832eca7c7d301ec4253e47ee42527aa617bac`  
		Last Modified: Mon, 10 May 2021 23:40:59 GMT  
		Size: 1.2 MB (1201547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e70f326991067a04529de021321ce20d6920e81d14aaef93afb92136c976508`  
		Last Modified: Mon, 10 May 2021 23:40:58 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:58ffe092c4ccbd15cf9faf25d63caa632bb639d53188a377038834ebf2dac85a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.6 MB (110621059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2321e3937c686734c8c9124a34811d9eb4092b7611145be19ea453a5bbb389a4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:30:57 GMT
ADD file:52162c4413e3597dad4ccb790c379b67ef40d50c0d0659e8b6c65d833886b3af in / 
# Wed, 14 Apr 2021 19:31:02 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 22:53:57 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 22:54:09 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 22:54:14 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 May 2021 00:22:47 GMT
ENV GOLANG_VERSION=1.16.4
# Fri, 07 May 2021 00:25:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 	sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Fri, 07 May 2021 00:25:26 GMT
ENV GOPATH=/go
# Fri, 07 May 2021 00:25:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 May 2021 00:25:58 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 07 May 2021 00:26:14 GMT
WORKDIR /go
# Fri, 07 May 2021 08:19:51 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 08:19:57 GMT
ENV XCADDY_VERSION=v0.1.9
# Tue, 11 May 2021 01:19:13 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 01:19:18 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 11 May 2021 01:19:27 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Tue, 11 May 2021 01:19:30 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Tue, 11 May 2021 01:19:37 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:771d2590aa602a0d4a922e322f02b22cc9d193f8cd159d9d1a140cadf1f8b4d4`  
		Last Modified: Wed, 14 Apr 2021 19:32:33 GMT  
		Size: 2.8 MB (2813141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf726c40dc4802009a4b6f0f7947c86242c2c078623e8f1f21343864093b3a9`  
		Last Modified: Wed, 14 Apr 2021 23:05:31 GMT  
		Size: 283.4 KB (283413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c17712dac96942b05a27f88ea5346bd57b4cabdb33c153562ef144635225b3`  
		Last Modified: Wed, 14 Apr 2021 23:05:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d2e93731067b7b48232c826d062ff4fead572dbd98e0a28642db4802342a8e`  
		Last Modified: Fri, 07 May 2021 00:41:39 GMT  
		Size: 99.5 MB (99528032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca0e521f95ca5f22fdd4b7917d06aead7df46288885c4fd3ffac0242b96643f`  
		Last Modified: Fri, 07 May 2021 00:41:14 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9dfa7e81a349fea3e170fbc6f6b9fd3245ee43c53b329a3ae72c9e5ebaddfb`  
		Last Modified: Fri, 07 May 2021 08:22:18 GMT  
		Size: 6.8 MB (6825232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87f3bfd07b70b357098f4ba50744bf3c838e8c3ab709598b79864f29b676311`  
		Last Modified: Tue, 11 May 2021 01:20:23 GMT  
		Size: 1.2 MB (1170526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68dce6545308f135393f568603954610d88f7a8a61ca402820d75500d925926c`  
		Last Modified: Tue, 11 May 2021 01:20:23 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - linux; s390x

```console
$ docker pull caddy@sha256:e72252e76203d04b2ed847e26d71ca0de7ed89c2d76990ac177fb80755d88617
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115474412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b08b1e73df9c564bfdb9249c0d32c47642dd69cd88bfa280b4682767ef8fe671`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:35 GMT
ADD file:c715fef757fe2b022ae1bbff71dbc58bddf5a858deb0aac5a6fbcf10d5f3111c in / 
# Wed, 14 Apr 2021 18:41:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:45:11 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 14 Apr 2021 20:45:11 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Apr 2021 20:45:11 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:16:38 GMT
ENV GOLANG_VERSION=1.16.4
# Thu, 06 May 2021 23:20:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		gnupg 		go 		musl-dev 		openssl 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			export GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$apkArch' (likely packaging update needed)"; exit 1 ;; 	esac; 		url='https://dl.google.com/go/go1.16.4.src.tar.gz'; 	sha256='ae4f6b6e2a1677d31817984655a762074b5356da50fb58722b99104870d43503'; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC EC91 7721 F63B D38B 4796'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		( 		cd /usr/local/go/src; 		export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 		if [ "${GO386:-}" = 'softfloat' ]; then 			GO386= ./bootstrap.bash; 			export GOROOT_BOOTSTRAP="/usr/local/go-$GOOS-$GOARCH-bootstrap"; 			"$GOROOT_BOOTSTRAP/bin/go" version; 		fi; 		./make.bash; 		if [ "${GO386:-}" = 'softfloat' ]; then 			rm -rf "$GOROOT_BOOTSTRAP"; 		fi; 	); 		apk del --no-network .build-deps; 		go install std; 		rm -rf 		/usr/local/go/pkg/*/cmd 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 		/usr/local/go/pkg/tool/*/api 		/usr/local/go/pkg/tool/*/go_bootstrap 		/usr/local/go/src/cmd/dist/dist 	; 		go version
# Thu, 06 May 2021 23:20:18 GMT
ENV GOPATH=/go
# Thu, 06 May 2021 23:20:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 23:20:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Thu, 06 May 2021 23:20:21 GMT
WORKDIR /go
# Fri, 07 May 2021 02:02:34 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 07 May 2021 02:02:35 GMT
ENV XCADDY_VERSION=v0.1.9
# Mon, 10 May 2021 23:42:03 GMT
ENV CADDY_VERSION=v2.4.0
# Mon, 10 May 2021 23:42:03 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 10 May 2021 23:42:05 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='8b36aa88d294cfd47e2bbba24d99559a5327db84de0a0b3c28e9f2c8e7c9df16bef96ca0cf033e6304474b7d94336843ee9665bf5159815ecac7986e3ee508bf' ;; 		armhf)   binArch='armv6'; checksum='7f8711d98e42ab6fb96fd7405df34944bcc97b16eab7c3d45fd8b496f690bed5cf041cc694b5b615fd88f91e87f75995501c484021f0d510b61375b6888efcc5' ;; 		armv7)   binArch='armv7'; checksum='adf762a2c765c84a933ad2b1b27609f3bf1b2394587cd9b199c661b02eea8783a7910b4dced1f8fd6bd33761a7ca792e1328f6acf54d9e4772922d095e541709' ;; 		aarch64) binArch='arm64'; checksum='4b914ffb89e0cacbac3d2dcf8e0db4682939d27d64160191f6941ba80dbb439e4d06d511ec6fefd1969a51895cdbd7b10dc0737efb13250ce9a03b39ae5cc6d3' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='e4bd087f7e9df1973af14fc420211976cdb34111349d36ad5e1bc193312bf076fc9fad8ce58ebdf09f9d7ff94017ce9dbab7c10fea1c0719ca26b9dc0cac5559' ;; 		s390x)   binArch='s390x'; checksum='4e2d075a0fa326683a4911dddcd0776f9de828645c602b9cdf1a6998c438ef265b6d4bb1ce85ef14de2064d7b2d730d36220fdff231674d67df33205ff3eec0b' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Mon, 10 May 2021 23:42:06 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Mon, 10 May 2021 23:42:06 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:afadee6ad6a38d3172beeeca818219604c782efbe93201ef4d39512f289b05ae`  
		Last Modified: Wed, 14 Apr 2021 18:42:16 GMT  
		Size: 2.6 MB (2602650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc746875ae346ee6ec3c9080f8a7a50bef3899ea9d5ae9dac45a81bfe861c9d`  
		Last Modified: Wed, 14 Apr 2021 20:52:25 GMT  
		Size: 281.7 KB (281708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0242688236000dd8f33d16f89f36da3ef1bb2a7a32bb59a7eb97a18ed3d5158`  
		Last Modified: Wed, 14 Apr 2021 20:52:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37dab17b6808078a43afd3d62f1a202857192406e914c33d5ceb5eec1eb05eeb`  
		Last Modified: Thu, 06 May 2021 23:34:08 GMT  
		Size: 104.8 MB (104849388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6059cb089a1bd1108012ddff056f297d814995f95d29d57b15c13d11baede00d`  
		Last Modified: Thu, 06 May 2021 23:33:52 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84919c1c43955cfb518f179d4f6b541cdfa94579f6f6ef10fdc6e6b3ca4d51a3`  
		Last Modified: Fri, 07 May 2021 02:03:18 GMT  
		Size: 6.5 MB (6475416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3025f5e46ec68c9ef05a49a22ca89718a0d154f401122b0505a18d1c9217fc`  
		Last Modified: Mon, 10 May 2021 23:42:38 GMT  
		Size: 1.3 MB (1264531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19bb5d9c7e67f1492e82b3f7c19e6900095d43b1f65fa5496f752a95169cd953`  
		Last Modified: Mon, 10 May 2021 23:42:38 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.17763.1879; amd64

```console
$ docker pull caddy@sha256:bc783b828c95b331d7fad4be39c04af02ab0b76ff396546a2d118771441f398e
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2641373061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed813a8f2c9cd1366b5455eb1fd1c585aa4ab0f42e380f58cb6a58f23c27eead`
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
# Thu, 06 May 2021 21:02:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 06 May 2021 21:02:30 GMT
ENV XCADDY_VERSION=v0.1.9
# Tue, 11 May 2021 00:22:36 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 00:22:38 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 11 May 2021 00:23:12 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d03d5f6e22cc1c7dfbfd7ca0946a1c313e6b7cf24eb846b4a732452445cede8ec1a3caff6d78b4ba6a47f8dfcfc85d989beb1165e5b74c230eabb0d20a3c6379')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 11 May 2021 00:23:13 GMT
WORKDIR C:\
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
	-	`sha256:8f6d89568ee8ac19213ae2e66b14601f80c6dd3c4a1205da5fa55da7003cd3a0`  
		Last Modified: Thu, 06 May 2021 21:06:02 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0aa20834bcdb38f731b9f6528281005b29ae951a02ef46190bf1be1cab5946`  
		Last Modified: Thu, 06 May 2021 21:06:00 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada218f8f73674eea11444ee4fa8048f2cfd6e2bfc8f8c2bb4cc40954436b6b0`  
		Last Modified: Tue, 11 May 2021 00:27:19 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815ac3cbadfa3d6463be2a02130f663d74e486df33a07b582def59fe66dd48b0`  
		Last Modified: Tue, 11 May 2021 00:27:19 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da0a5d30891cb84455c6b13f7a6b778a19b3a271813ef7066eb0ba908192ee7`  
		Last Modified: Tue, 11 May 2021 00:27:20 GMT  
		Size: 1.7 MB (1738012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882e2cb2540135f046b5adb4957a0f75118aeb15e30d46af750522a16e6f0cc2`  
		Last Modified: Tue, 11 May 2021 00:27:19 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder` - windows version 10.0.14393.4350; amd64

```console
$ docker pull caddy@sha256:1b2ba73c8dc7fce225f65c457524b3830589cf0fa3e9c62faa0c88b15c73c74f
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5987368241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd19fd51f0fc365a83899a16ab9d8fb86585a512ff6cc33bd07e7af1bc5d89d4`
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
# Thu, 06 May 2021 21:03:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 06 May 2021 21:03:07 GMT
ENV XCADDY_VERSION=v0.1.9
# Tue, 11 May 2021 00:23:23 GMT
ENV CADDY_VERSION=v2.4.0
# Tue, 11 May 2021 00:23:24 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 11 May 2021 00:25:06 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.1.9/xcaddy_0.1.9_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('d03d5f6e22cc1c7dfbfd7ca0946a1c313e6b7cf24eb846b4a732452445cede8ec1a3caff6d78b4ba6a47f8dfcfc85d989beb1165e5b74c230eabb0d20a3c6379')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 11 May 2021 00:25:08 GMT
WORKDIR C:\
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
	-	`sha256:bee5214a4bbf455290910bf5850bebdd3fdde0c4bf2616c2975a8a91b62cfe7a`  
		Last Modified: Thu, 06 May 2021 21:06:13 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f9311ef107812e0fc28e80ff17843a7d95e33d9b4311d0ff921022f5d199c3`  
		Last Modified: Thu, 06 May 2021 21:06:10 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b921e314d8bdd24486247a7d82137f437b1572bec858ea76813dc27e580670`  
		Last Modified: Tue, 11 May 2021 00:27:35 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8450625dd9bbf2232b7a3d1cbce4d8795d03b140b1fb962bb6042b82a073633`  
		Last Modified: Tue, 11 May 2021 00:27:35 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:394074991c1e1b9a6750cf551fb9f7fe9eaffa1a25889bebcf0f35682cb69afe`  
		Last Modified: Tue, 11 May 2021 00:27:37 GMT  
		Size: 7.0 MB (6993409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5f2fa898b0d7f2684b17b889c9c68aa767c0a1f408e2e4eceb3374cdf48393`  
		Last Modified: Tue, 11 May 2021 00:27:35 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
