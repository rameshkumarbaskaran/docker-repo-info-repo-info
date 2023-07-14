## `caddy:2-builder-alpine`

```console
$ docker pull caddy@sha256:1fe33ca93062345cec28685866fc3d65b413b0878537989b7afc953cf3eb79cf
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
$ docker pull caddy@sha256:0458a6633430f81251ddd89d9224edcd9d2f55c937673d9fbb68c76132d3e82b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132406721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4b406493fef136adf72abe568f6303eb2b44bab3e65ee07933b8b6ed504a7ff`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 22:35:02 GMT
RUN apk add --no-cache ca-certificates
# Wed, 14 Jun 2023 22:35:02 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Jul 2023 19:24:20 GMT
ENV GOLANG_VERSION=1.19.11
# Thu, 13 Jul 2023 20:33:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.11.src.tar.gz'; 		sha256='e25c9ab72d811142b7f41ff6da5165fec2d1be5feec3ef2c66bc0bdecb431489'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 13 Jul 2023 20:33:56 GMT
ENV GOPATH=/go
# Thu, 13 Jul 2023 20:33:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jul 2023 20:33:56 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Thu, 13 Jul 2023 20:33:57 GMT
WORKDIR /go
# Thu, 13 Jul 2023 22:11:26 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Thu, 13 Jul 2023 22:11:26 GMT
ENV XCADDY_VERSION=v0.3.4
# Thu, 13 Jul 2023 22:11:26 GMT
ENV CADDY_VERSION=v2.6.4
# Thu, 13 Jul 2023 22:11:26 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 13 Jul 2023 22:11:27 GMT
ENV XCADDY_SETCAP=1
# Thu, 13 Jul 2023 22:11:28 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='68ab15d90eb70c23e8b13c3935b194fc1b638f8c0fee6506a109dcee082c20d6e07890320a876b13eb23b5a7a0617daa28fe8af24dcb0dcb3eca9ea74dc76713' ;; 		armhf)   binArch='armv6'; checksum='2853413e63ac29f296b1c44696022febc8b29c4b37fb20442b635903a0b79d523ca00896dfce3e40f5894dd297b345ac007af0ddffccaada843c7de61d334134' ;; 		armv7)   binArch='armv7'; checksum='c59e93ba270705b2312f6a70552f2a345cec91cc3504233785cb46fa4b644a47e520bb29dfbf519f814bb13d0bbea213976fd7b059883eab2b091913f9ed393f' ;; 		aarch64) binArch='arm64'; checksum='df4c58e97931ca58b7a38d245948912b817e952a2961ff583744039ca68a584a303f7cbfdb33392c84d8f76f5b30f206d9f84a04f547043a3d1fa5282b0fd544' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2795d5b7546bd10ff3cd21a393597281e42e1043164536e01e18fb56047ba5b396493a086bb2d90e8ede9a54b5208e947ecaacccca4a8550704fb3f8a17dd771' ;; 		s390x)   binArch='s390x'; checksum='2ed85231aac36e3af873e3fdf4f6b6378b55dcc17743d24b28b3b48d6622fde73aae58eed124082478a0b841c338d64caa0b0be302545a79092a97cf205f1b29' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.4/xcaddy_0.3.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 13 Jul 2023 22:11:28 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 13 Jul 2023 22:11:28 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9bcf943fa5571df036dca6da19434d38edf546ef8bb04ddbc803634cc9a3b8`  
		Last Modified: Wed, 14 Jun 2023 22:42:14 GMT  
		Size: 284.7 KB (284706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ecaf4eb86ef9fd3ad1377b7cf4882dccebd4c639d427e246a275ddcd4c53bf`  
		Last Modified: Thu, 13 Jul 2023 20:38:32 GMT  
		Size: 122.5 MB (122464754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1f0b61d268d8a27e49e488a5a8b578c5f11f5929e83313ea400d1a268d6358`  
		Last Modified: Thu, 13 Jul 2023 20:38:17 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e7a25f2f0dce0a79650117fb4a1eb185ad59c9e43d0c298cae1a77cd4c6791`  
		Last Modified: Thu, 13 Jul 2023 22:12:00 GMT  
		Size: 5.0 MB (4957605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfae2eb5f7df4c15fe0b2bae6eae3a3c131061176bf0ee509a84f110fa3a4f1a`  
		Last Modified: Thu, 13 Jul 2023 22:11:59 GMT  
		Size: 1.3 MB (1301217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7af916117dade0bc32bdb1be6637faffc6e2de3e98b52bd811a6726fd21e4a2`  
		Last Modified: Thu, 13 Jul 2023 22:11:59 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v6

```console
$ docker pull caddy@sha256:b7340bd2dc18da1dc7361481d407bf5c9a52bb0a40a328dea8fd7e5a19ad73fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128462417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71d2ba888c0c501b505945afb80de3ac29395710142d1a0183d98ed5a052507b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:20 GMT
ADD file:4213782693bf27a9a6de23bc924ef0c4fb6b2d56010fc07b25f81edeba83b0d4 in / 
# Wed, 14 Jun 2023 18:49:20 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 19:56:52 GMT
RUN apk add --no-cache ca-certificates
# Wed, 14 Jun 2023 19:56:52 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Jul 2023 19:07:38 GMT
ENV GOLANG_VERSION=1.19.11
# Thu, 13 Jul 2023 19:56:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.11.src.tar.gz'; 		sha256='e25c9ab72d811142b7f41ff6da5165fec2d1be5feec3ef2c66bc0bdecb431489'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 13 Jul 2023 19:56:09 GMT
ENV GOPATH=/go
# Thu, 13 Jul 2023 19:56:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jul 2023 19:56:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Thu, 13 Jul 2023 19:56:10 GMT
WORKDIR /go
# Thu, 13 Jul 2023 20:42:42 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Thu, 13 Jul 2023 20:42:42 GMT
ENV XCADDY_VERSION=v0.3.4
# Thu, 13 Jul 2023 20:42:42 GMT
ENV CADDY_VERSION=v2.6.4
# Thu, 13 Jul 2023 20:42:42 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 13 Jul 2023 20:42:42 GMT
ENV XCADDY_SETCAP=1
# Thu, 13 Jul 2023 20:42:44 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='68ab15d90eb70c23e8b13c3935b194fc1b638f8c0fee6506a109dcee082c20d6e07890320a876b13eb23b5a7a0617daa28fe8af24dcb0dcb3eca9ea74dc76713' ;; 		armhf)   binArch='armv6'; checksum='2853413e63ac29f296b1c44696022febc8b29c4b37fb20442b635903a0b79d523ca00896dfce3e40f5894dd297b345ac007af0ddffccaada843c7de61d334134' ;; 		armv7)   binArch='armv7'; checksum='c59e93ba270705b2312f6a70552f2a345cec91cc3504233785cb46fa4b644a47e520bb29dfbf519f814bb13d0bbea213976fd7b059883eab2b091913f9ed393f' ;; 		aarch64) binArch='arm64'; checksum='df4c58e97931ca58b7a38d245948912b817e952a2961ff583744039ca68a584a303f7cbfdb33392c84d8f76f5b30f206d9f84a04f547043a3d1fa5282b0fd544' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2795d5b7546bd10ff3cd21a393597281e42e1043164536e01e18fb56047ba5b396493a086bb2d90e8ede9a54b5208e947ecaacccca4a8550704fb3f8a17dd771' ;; 		s390x)   binArch='s390x'; checksum='2ed85231aac36e3af873e3fdf4f6b6378b55dcc17743d24b28b3b48d6622fde73aae58eed124082478a0b841c338d64caa0b0be302545a79092a97cf205f1b29' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.4/xcaddy_0.3.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 13 Jul 2023 20:42:44 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 13 Jul 2023 20:42:44 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:7836be94d3024e2042069c1095caba0b391f70c4b3d34a0475a503239d73dfba`  
		Last Modified: Wed, 14 Jun 2023 18:49:46 GMT  
		Size: 3.1 MB (3143353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ffe4223b1ef1f186378646830e3b2006e9e2e96241c0b319c50387ac3fa566`  
		Last Modified: Wed, 14 Jun 2023 20:08:03 GMT  
		Size: 284.9 KB (284873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04858a4a47412563c68840d2b52f172d33236dcc3cbbfa1e369b7cf4a3b809f6`  
		Last Modified: Thu, 13 Jul 2023 20:01:19 GMT  
		Size: 118.8 MB (118836203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a764178f97c2898539ecc0ae6a06cc851a8182e8a379e4c8fa6404b87a49c1`  
		Last Modified: Thu, 13 Jul 2023 20:00:59 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e383ca5293d5adc3172bdac5e60e13484d4a1a3437f2c759e9c6f8e2bc916a`  
		Last Modified: Thu, 13 Jul 2023 20:43:11 GMT  
		Size: 5.0 MB (4950283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90f38b4bb392be48b89a4296f1c64e785b3ad52d0f87d54d8c6890103776d9c1`  
		Last Modified: Thu, 13 Jul 2023 20:43:10 GMT  
		Size: 1.2 MB (1247144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8a34bfba2395f02d77bba6a058cfc9014485fd1b57035fabb4d4147ad7780e`  
		Last Modified: Thu, 13 Jul 2023 20:43:10 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm variant v7

```console
$ docker pull caddy@sha256:51cd0a16f094d56869423243a67efb0ce1cc525a0baf4b09f553886c71ea2a22
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127513812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b085d31bf96bf489dbed26dc745092995ad7a837659e38f0455ce94050d0b80e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Jun 2023 22:36:15 GMT
ADD file:082f034323c559f3cb9feb6422c88b1ec8017f436d6109e238a5c5384a32a90a in / 
# Wed, 14 Jun 2023 22:36:15 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 02:14:54 GMT
RUN apk add --no-cache ca-certificates
# Thu, 15 Jun 2023 02:14:54 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Jul 2023 19:19:08 GMT
ENV GOLANG_VERSION=1.19.11
# Thu, 13 Jul 2023 20:06:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.11.src.tar.gz'; 		sha256='e25c9ab72d811142b7f41ff6da5165fec2d1be5feec3ef2c66bc0bdecb431489'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 13 Jul 2023 20:06:19 GMT
ENV GOPATH=/go
# Thu, 13 Jul 2023 20:06:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jul 2023 20:06:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Thu, 13 Jul 2023 20:06:21 GMT
WORKDIR /go
# Thu, 13 Jul 2023 22:14:20 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Thu, 13 Jul 2023 22:14:20 GMT
ENV XCADDY_VERSION=v0.3.4
# Thu, 13 Jul 2023 22:14:20 GMT
ENV CADDY_VERSION=v2.6.4
# Thu, 13 Jul 2023 22:14:21 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 13 Jul 2023 22:14:21 GMT
ENV XCADDY_SETCAP=1
# Thu, 13 Jul 2023 22:14:22 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='68ab15d90eb70c23e8b13c3935b194fc1b638f8c0fee6506a109dcee082c20d6e07890320a876b13eb23b5a7a0617daa28fe8af24dcb0dcb3eca9ea74dc76713' ;; 		armhf)   binArch='armv6'; checksum='2853413e63ac29f296b1c44696022febc8b29c4b37fb20442b635903a0b79d523ca00896dfce3e40f5894dd297b345ac007af0ddffccaada843c7de61d334134' ;; 		armv7)   binArch='armv7'; checksum='c59e93ba270705b2312f6a70552f2a345cec91cc3504233785cb46fa4b644a47e520bb29dfbf519f814bb13d0bbea213976fd7b059883eab2b091913f9ed393f' ;; 		aarch64) binArch='arm64'; checksum='df4c58e97931ca58b7a38d245948912b817e952a2961ff583744039ca68a584a303f7cbfdb33392c84d8f76f5b30f206d9f84a04f547043a3d1fa5282b0fd544' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2795d5b7546bd10ff3cd21a393597281e42e1043164536e01e18fb56047ba5b396493a086bb2d90e8ede9a54b5208e947ecaacccca4a8550704fb3f8a17dd771' ;; 		s390x)   binArch='s390x'; checksum='2ed85231aac36e3af873e3fdf4f6b6378b55dcc17743d24b28b3b48d6622fde73aae58eed124082478a0b841c338d64caa0b0be302545a79092a97cf205f1b29' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.4/xcaddy_0.3.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 13 Jul 2023 22:14:22 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 13 Jul 2023 22:14:22 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:633ba29fd335042456b6e2c073636f6fa30de56f1331c442914739b92a479974`  
		Last Modified: Wed, 14 Jun 2023 22:36:49 GMT  
		Size: 2.9 MB (2898508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad2d22fcfeec0ce3f819b7931d5f6b12f8aa5ed452de9e2200f594a3bacfa30`  
		Last Modified: Thu, 15 Jun 2023 02:23:48 GMT  
		Size: 284.1 KB (284075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db530994f93ec024f821818fbd874576f0d879bea6ea8a1d0c916bacc87b4b0`  
		Last Modified: Thu, 13 Jul 2023 20:11:23 GMT  
		Size: 118.6 MB (118585300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:105518b3e6d3c6a6bc8123597aae9b7b74115353d42079ec36b2e8ddefe3177a`  
		Last Modified: Thu, 13 Jul 2023 20:11:05 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53005af44d40b207150ac0bd48a7fc521f6df3ca6f1f55cf7081a4caadf6a15b`  
		Last Modified: Thu, 13 Jul 2023 22:14:50 GMT  
		Size: 4.5 MB (4500133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d2e3be2ebfbe71c5346068b03834e37e9a0fd700afd1c2583ed276f138b6c9`  
		Last Modified: Thu, 13 Jul 2023 22:14:50 GMT  
		Size: 1.2 MB (1245239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e366a08a09c7045454df88aef5277a8024fa5f499f1ef4add4e6e6da613e2fba`  
		Last Modified: Thu, 13 Jul 2023 22:14:50 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:fa21fb2f38c10dfc70971fba0fae05e7dbd903e03ed1b0e57f55cc3621a7dd72
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126904491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b66901b0452a17981dd7189bc550c3725c7bbdf2605c84a2878495cd856d5076`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 23:22:17 GMT
RUN apk add --no-cache ca-certificates
# Wed, 14 Jun 2023 23:22:17 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Jul 2023 19:15:54 GMT
ENV GOLANG_VERSION=1.19.11
# Thu, 13 Jul 2023 20:43:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.11.src.tar.gz'; 		sha256='e25c9ab72d811142b7f41ff6da5165fec2d1be5feec3ef2c66bc0bdecb431489'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 13 Jul 2023 20:43:49 GMT
ENV GOPATH=/go
# Thu, 13 Jul 2023 20:43:49 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jul 2023 20:43:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Thu, 13 Jul 2023 20:43:49 GMT
WORKDIR /go
# Thu, 13 Jul 2023 22:39:06 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Thu, 13 Jul 2023 22:39:06 GMT
ENV XCADDY_VERSION=v0.3.4
# Thu, 13 Jul 2023 22:39:06 GMT
ENV CADDY_VERSION=v2.6.4
# Thu, 13 Jul 2023 22:39:06 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 13 Jul 2023 22:39:06 GMT
ENV XCADDY_SETCAP=1
# Thu, 13 Jul 2023 22:39:07 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='68ab15d90eb70c23e8b13c3935b194fc1b638f8c0fee6506a109dcee082c20d6e07890320a876b13eb23b5a7a0617daa28fe8af24dcb0dcb3eca9ea74dc76713' ;; 		armhf)   binArch='armv6'; checksum='2853413e63ac29f296b1c44696022febc8b29c4b37fb20442b635903a0b79d523ca00896dfce3e40f5894dd297b345ac007af0ddffccaada843c7de61d334134' ;; 		armv7)   binArch='armv7'; checksum='c59e93ba270705b2312f6a70552f2a345cec91cc3504233785cb46fa4b644a47e520bb29dfbf519f814bb13d0bbea213976fd7b059883eab2b091913f9ed393f' ;; 		aarch64) binArch='arm64'; checksum='df4c58e97931ca58b7a38d245948912b817e952a2961ff583744039ca68a584a303f7cbfdb33392c84d8f76f5b30f206d9f84a04f547043a3d1fa5282b0fd544' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2795d5b7546bd10ff3cd21a393597281e42e1043164536e01e18fb56047ba5b396493a086bb2d90e8ede9a54b5208e947ecaacccca4a8550704fb3f8a17dd771' ;; 		s390x)   binArch='s390x'; checksum='2ed85231aac36e3af873e3fdf4f6b6378b55dcc17743d24b28b3b48d6622fde73aae58eed124082478a0b841c338d64caa0b0be302545a79092a97cf205f1b29' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.4/xcaddy_0.3.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 13 Jul 2023 22:39:07 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 13 Jul 2023 22:39:08 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a768fa670f57b0faf1a0a8cb211432ed97307628729fa53e3ea9981ba7512d4`  
		Last Modified: Wed, 14 Jun 2023 23:27:58 GMT  
		Size: 286.3 KB (286290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ad8919c69a4809ea86f90260db4395f9fa62cd06abc3db2a283629ae87bcfd`  
		Last Modified: Thu, 13 Jul 2023 20:47:52 GMT  
		Size: 117.0 MB (117037222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ab6a7950ae623a053f628d5a9c1445ab6892c276ce29cd3e61f7abef6a98c8`  
		Last Modified: Thu, 13 Jul 2023 20:47:39 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec72f273e241b81df74f6002153830f789bb54a868995dea6d9ae9d5d27cd3e`  
		Last Modified: Thu, 13 Jul 2023 22:39:33 GMT  
		Size: 5.1 MB (5053701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa4944f7d930e5c879ed1af714ff93de7266ed9486997ef52108bf966360b45`  
		Last Modified: Thu, 13 Jul 2023 22:39:32 GMT  
		Size: 1.2 MB (1197467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6a0fe15b61b065ce8771327d6582dbdb390b8fbc1f5c8ad61ec093ab94e6a2`  
		Last Modified: Thu, 13 Jul 2023 22:39:32 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; ppc64le

```console
$ docker pull caddy@sha256:6f0a370b7e56f9e0a5b4c9f349ef1be1dfb7638fac22bff766c298246217ef14
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127484405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ad40bb34e9b7d5a3d640f116aeb49e6e5477d58fe35c601c6f710cccb2ba99`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 15 Jun 2023 00:39:49 GMT
ADD file:694c636c0dd19fd01accbc189e4c1dc4d063952692c6e7eb26dce02a7adba833 in / 
# Thu, 15 Jun 2023 00:39:49 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 01:25:57 GMT
RUN apk add --no-cache ca-certificates
# Thu, 15 Jun 2023 01:25:57 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Jul 2023 19:12:27 GMT
ENV GOLANG_VERSION=1.19.11
# Thu, 13 Jul 2023 20:26:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.11.src.tar.gz'; 		sha256='e25c9ab72d811142b7f41ff6da5165fec2d1be5feec3ef2c66bc0bdecb431489'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 13 Jul 2023 20:26:47 GMT
ENV GOPATH=/go
# Thu, 13 Jul 2023 20:26:47 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jul 2023 20:26:49 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Thu, 13 Jul 2023 20:26:49 GMT
WORKDIR /go
# Thu, 13 Jul 2023 23:47:08 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Thu, 13 Jul 2023 23:47:09 GMT
ENV XCADDY_VERSION=v0.3.4
# Thu, 13 Jul 2023 23:47:10 GMT
ENV CADDY_VERSION=v2.6.4
# Thu, 13 Jul 2023 23:47:12 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 13 Jul 2023 23:47:13 GMT
ENV XCADDY_SETCAP=1
# Thu, 13 Jul 2023 23:47:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='68ab15d90eb70c23e8b13c3935b194fc1b638f8c0fee6506a109dcee082c20d6e07890320a876b13eb23b5a7a0617daa28fe8af24dcb0dcb3eca9ea74dc76713' ;; 		armhf)   binArch='armv6'; checksum='2853413e63ac29f296b1c44696022febc8b29c4b37fb20442b635903a0b79d523ca00896dfce3e40f5894dd297b345ac007af0ddffccaada843c7de61d334134' ;; 		armv7)   binArch='armv7'; checksum='c59e93ba270705b2312f6a70552f2a345cec91cc3504233785cb46fa4b644a47e520bb29dfbf519f814bb13d0bbea213976fd7b059883eab2b091913f9ed393f' ;; 		aarch64) binArch='arm64'; checksum='df4c58e97931ca58b7a38d245948912b817e952a2961ff583744039ca68a584a303f7cbfdb33392c84d8f76f5b30f206d9f84a04f547043a3d1fa5282b0fd544' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2795d5b7546bd10ff3cd21a393597281e42e1043164536e01e18fb56047ba5b396493a086bb2d90e8ede9a54b5208e947ecaacccca4a8550704fb3f8a17dd771' ;; 		s390x)   binArch='s390x'; checksum='2ed85231aac36e3af873e3fdf4f6b6378b55dcc17743d24b28b3b48d6622fde73aae58eed124082478a0b841c338d64caa0b0be302545a79092a97cf205f1b29' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.4/xcaddy_0.3.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 13 Jul 2023 23:47:17 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 13 Jul 2023 23:47:18 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:ffa4a466dbb8eebd7e7f25590a9df12390de9016abf82279c29c9a64aa76491a`  
		Last Modified: Thu, 15 Jun 2023 00:40:26 GMT  
		Size: 3.3 MB (3344781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1647fd337167bcedcd03fcbbea1cdda0214e39f0c809960a10a1a2e7f5ec905`  
		Last Modified: Thu, 15 Jun 2023 01:37:59 GMT  
		Size: 286.7 KB (286671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe7bde47480a9b8d12aa0b23c01af4705608ad0b33742696b9133d628d7ccce4`  
		Last Modified: Thu, 13 Jul 2023 20:34:10 GMT  
		Size: 117.4 MB (117417564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76dceb42661cd838f2ea5fc3fe33ae4afb40014d16e77062fe6bbc059b1cea2e`  
		Last Modified: Thu, 13 Jul 2023 20:33:44 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54027f403d95282aecf5bcd8eec158b4fe0986e97c4bbf5feadd8df6caac87c`  
		Last Modified: Thu, 13 Jul 2023 23:48:15 GMT  
		Size: 5.2 MB (5249633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18c6920aaccaf484b3b905e413f4c0fdfff1a9b794ccf52415307e9db7302a7`  
		Last Modified: Thu, 13 Jul 2023 23:48:14 GMT  
		Size: 1.2 MB (1185194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a3d2ddab01cf5460d8f933421b8c4970a30522d992e6152abb851a65ec24b2`  
		Last Modified: Thu, 13 Jul 2023 23:48:13 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:2-builder-alpine` - linux; s390x

```console
$ docker pull caddy@sha256:20afa33b9e4aee20b87bdf3f1da3a22a3d8a6878f5f9d49ee35ec30e2cb84450
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 MB (130769215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d183ef8cac47ea38bba53eede1b843eac5d3a5a9d709ffa92dd933b67e3c2170`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 15 Jun 2023 05:18:38 GMT
ADD file:a59beca78118ebf4f86cc1685237dc3a29a519401a70668da520beaa3d29eb7a in / 
# Thu, 15 Jun 2023 05:18:38 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 05:37:10 GMT
RUN apk add --no-cache ca-certificates
# Thu, 15 Jun 2023 05:37:10 GMT
ENV PATH=/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Jul 2023 19:48:06 GMT
ENV GOLANG_VERSION=1.19.11
# Thu, 13 Jul 2023 21:22:44 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps gnupg; 	arch="$(apk --print-arch)"; 	url=; 	case "$arch" in 		'x86_64') 			export GOAMD64='v1' GOARCH='amd64' GOOS='linux'; 			;; 		'armhf') 			export GOARCH='arm' GOARM='6' GOOS='linux'; 			;; 		'armv7') 			export GOARCH='arm' GOARM='7' GOOS='linux'; 			;; 		'aarch64') 			export GOARCH='arm64' GOOS='linux'; 			;; 		'x86') 			export GO386='softfloat' GOARCH='386' GOOS='linux'; 			;; 		'ppc64le') 			export GOARCH='ppc64le' GOOS='linux'; 			;; 		'riscv64') 			export GOARCH='riscv64' GOOS='linux'; 			;; 		's390x') 			export GOARCH='s390x' GOOS='linux'; 			;; 		*) echo >&2 "error: unsupported architecture '$arch' (likely packaging update needed)"; exit 1 ;; 	esac; 	build=; 	if [ -z "$url" ]; then 		build=1; 		url='https://dl.google.com/go/go1.19.11.src.tar.gz'; 		sha256='e25c9ab72d811142b7f41ff6da5165fec2d1be5feec3ef2c66bc0bdecb431489'; 	fi; 		wget -O go.tgz.asc "$url.asc"; 	wget -O go.tgz "$url"; 	echo "$sha256 *go.tgz" | sha256sum -c -; 		GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 'EB4C 1BFD 4F04 2F6D DDCC  EC91 7721 F63B D38B 4796'; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys '2F52 8D36 D67B 69ED F998  D857 78BD 6547 3CB3 BD13'; 	gpg --batch --verify go.tgz.asc go.tgz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" go.tgz.asc; 		tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		if [ -n "$build" ]; then 		apk add --no-cache --virtual .build-deps 			bash 			gcc 			go 			musl-dev 		; 				export GOCACHE='/tmp/gocache'; 				( 			cd /usr/local/go/src; 			export GOROOT_BOOTSTRAP="$(go env GOROOT)" GOHOSTOS="$GOOS" GOHOSTARCH="$GOARCH"; 			if [ "${GOARCH:-}" = '386' ]; then 				export CGO_CFLAGS='-fno-stack-protector'; 			fi; 			./make.bash; 		); 				apk del --no-network .build-deps; 				rm -rf 			/usr/local/go/pkg/*/cmd 			/usr/local/go/pkg/bootstrap 			/usr/local/go/pkg/obj 			/usr/local/go/pkg/tool/*/api 			/usr/local/go/pkg/tool/*/go_bootstrap 			/usr/local/go/src/cmd/dist/dist 			"$GOCACHE" 		; 	fi; 		apk del --no-network .fetch-deps; 		go version
# Thu, 13 Jul 2023 21:22:51 GMT
ENV GOPATH=/go
# Thu, 13 Jul 2023 21:22:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jul 2023 21:22:52 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH"
# Thu, 13 Jul 2023 21:22:52 GMT
WORKDIR /go
# Thu, 13 Jul 2023 21:43:36 GMT
RUN apk add --no-cache 	ca-certificates 	git 	libcap
# Thu, 13 Jul 2023 21:43:36 GMT
ENV XCADDY_VERSION=v0.3.4
# Thu, 13 Jul 2023 21:43:37 GMT
ENV CADDY_VERSION=v2.6.4
# Thu, 13 Jul 2023 21:43:37 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 13 Jul 2023 21:43:37 GMT
ENV XCADDY_SETCAP=1
# Thu, 13 Jul 2023 21:43:38 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  binArch='amd64'; checksum='68ab15d90eb70c23e8b13c3935b194fc1b638f8c0fee6506a109dcee082c20d6e07890320a876b13eb23b5a7a0617daa28fe8af24dcb0dcb3eca9ea74dc76713' ;; 		armhf)   binArch='armv6'; checksum='2853413e63ac29f296b1c44696022febc8b29c4b37fb20442b635903a0b79d523ca00896dfce3e40f5894dd297b345ac007af0ddffccaada843c7de61d334134' ;; 		armv7)   binArch='armv7'; checksum='c59e93ba270705b2312f6a70552f2a345cec91cc3504233785cb46fa4b644a47e520bb29dfbf519f814bb13d0bbea213976fd7b059883eab2b091913f9ed393f' ;; 		aarch64) binArch='arm64'; checksum='df4c58e97931ca58b7a38d245948912b817e952a2961ff583744039ca68a584a303f7cbfdb33392c84d8f76f5b30f206d9f84a04f547043a3d1fa5282b0fd544' ;; 		ppc64el|ppc64le) binArch='ppc64le'; checksum='2795d5b7546bd10ff3cd21a393597281e42e1043164536e01e18fb56047ba5b396493a086bb2d90e8ede9a54b5208e947ecaacccca4a8550704fb3f8a17dd771' ;; 		s390x)   binArch='s390x'; checksum='2ed85231aac36e3af873e3fdf4f6b6378b55dcc17743d24b28b3b48d6622fde73aae58eed124082478a0b841c338d64caa0b0be302545a79092a97cf205f1b29' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 	wget -O /tmp/xcaddy.tar.gz "https://github.com/caddyserver/xcaddy/releases/download/v0.3.4/xcaddy_0.3.4_linux_${binArch}.tar.gz"; 	echo "$checksum  /tmp/xcaddy.tar.gz" | sha512sum -c; 	tar x -z -f /tmp/xcaddy.tar.gz -C /usr/bin xcaddy; 	rm -f /tmp/xcaddy.tar.gz; 	chmod +x /usr/bin/xcaddy;
# Thu, 13 Jul 2023 21:43:38 GMT
COPY file:3284b89c053fa1b60b278653bdca42a092891284e07e11d2fe66ee30b14e3081 in /usr/bin/caddy-builder 
# Thu, 13 Jul 2023 21:43:38 GMT
WORKDIR /usr/bin
```

-	Layers:
	-	`sha256:998cc98447b44e5f0fe799dce691412796ba586ab22eb7c99aebf9d45f34833b`  
		Last Modified: Thu, 15 Jun 2023 05:29:38 GMT  
		Size: 3.2 MB (3213497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175521994a5932158dbd78d2153c38836ab5e1db0ceb4af91113d4c49c5caba2`  
		Last Modified: Thu, 15 Jun 2023 06:04:00 GMT  
		Size: 285.1 KB (285091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e82b599cdbed0ad1b5fa411c5cc09db9b7be42d548a6735843531940882ae7`  
		Last Modified: Thu, 13 Jul 2023 21:27:32 GMT  
		Size: 120.9 MB (120908969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065f8658be02ff204ec6aff0e5b001e14a0340a2bd94275069b923fe6c4ec75e`  
		Last Modified: Thu, 13 Jul 2023 21:27:17 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b2850fc756e6845a44aa48b6fe837af96097f551be8e4c0ce0d1420a02442e`  
		Last Modified: Thu, 13 Jul 2023 21:44:22 GMT  
		Size: 5.1 MB (5099695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da702f7598a86104738b06d561d98bcf9bd3ad0d1b3764ad6c9032d04b522a5`  
		Last Modified: Thu, 13 Jul 2023 21:44:21 GMT  
		Size: 1.3 MB (1261403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d735874bbecedd63659e5d01c02827f03732818cd971647640e4c93ced74b17`  
		Last Modified: Thu, 13 Jul 2023 21:44:21 GMT  
		Size: 405.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
