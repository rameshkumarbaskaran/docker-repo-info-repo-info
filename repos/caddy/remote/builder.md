## `caddy:builder`

```console
$ docker pull caddy@sha256:b9802bfc469494176b1e7b618dd7adbb7ef62fd2976aa80d6cb5a7413a562d1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `caddy:builder` - linux; amd64

```console
$ docker pull caddy@sha256:e36b8ed5c449779e0a1fa9ece869a502a844a21d3c246bec3c64f54e494ea80b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.2 MB (331168382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4952a0e367e3902096934f29eabb3b40146d64aaabfc533b08ec7df4295b681d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:30:19 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:30:20 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 17 Jul 2020 02:20:31 GMT
ENV GOLANG_VERSION=1.14.6
# Fri, 17 Jul 2020 02:22:44 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '73fc9d781815d411928eccb92bf20d5b4264797be69410eac854babe44c94c09 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 17 Jul 2020 02:22:45 GMT
ENV GOPATH=/go
# Fri, 17 Jul 2020 02:22:45 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Jul 2020 02:22:46 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 17 Jul 2020 02:22:46 GMT
WORKDIR /go
# Fri, 17 Jul 2020 02:50:22 GMT
WORKDIR /src
# Fri, 17 Jul 2020 02:50:24 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 17 Jul 2020 02:50:24 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Fri, 17 Jul 2020 02:50:26 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Fri, 17 Jul 2020 02:50:26 GMT
WORKDIR /src/caddy/cmd/caddy
# Fri, 17 Jul 2020 02:50:49 GMT
RUN go get -d ./...
# Fri, 17 Jul 2020 02:50:51 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Fri, 17 Jul 2020 02:50:51 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8968b2872e472e21554ca58b35a02277634f3e501cc04ab7b0d0963f60f54d`  
		Last Modified: Tue, 02 Jun 2020 01:44:13 GMT  
		Size: 282.6 KB (282603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92cc7c5fd73817407fa0e4de5e1fb262a9c0f34c35c7450a2d01a7cef79c62f`  
		Last Modified: Tue, 02 Jun 2020 01:44:14 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00abe362642d012af91b6be6c49d92940b67166682973d33b494ba7ded5a635a`  
		Last Modified: Fri, 17 Jul 2020 02:32:28 GMT  
		Size: 132.5 MB (132524788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0491c15e88ffef3bb5af8af7ac5aea412adb85ab1632b2bb89179132304df81`  
		Last Modified: Fri, 17 Jul 2020 02:32:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ab277974210fa40d65f8a717b614476cf2a00b95f1615f95af605e6dc8752a`  
		Last Modified: Fri, 17 Jul 2020 02:51:07 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ea3544be42ca4bacfead93d01b33949cc5729af5b7b16e5a2304561f2c4c6e`  
		Last Modified: Fri, 17 Jul 2020 02:51:08 GMT  
		Size: 8.3 MB (8310030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb55020dfbb96ed86536d3f3ee4cfe5d65c31fd943b084fb98411b1441c0a60`  
		Last Modified: Fri, 17 Jul 2020 02:51:06 GMT  
		Size: 3.0 MB (3020915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18cb4727040aafcb55500dc13aab52d4a34221462584428f46c21e41bc086495`  
		Last Modified: Fri, 17 Jul 2020 02:51:37 GMT  
		Size: 184.2 MB (184231468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64dd2f1035f3378ab0ca666ecef614fb9ce84c8374e6c48849db241bf74d92f7`  
		Last Modified: Fri, 17 Jul 2020 02:51:05 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74308353d5e0db8661ab6a54f64c651aaa60c78e229fdd8855c7514dccf02eed`  
		Last Modified: Fri, 17 Jul 2020 02:51:06 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v6

```console
$ docker pull caddy@sha256:5aac504dfa69ae0d2e73710818fab4b22ff75ad9529925e2146f830c221e9f24
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.7 MB (326700982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:998072aa467f0a36276dc5ea6797721af7ee251a35e93f2b04e47294657e40d9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:50:55 GMT
ADD file:f46e997a56849423db17e5fc9f0249ab6c73b155245927dba5fcb9dfd65f622f in / 
# Fri, 29 May 2020 21:50:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 02:02:10 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 02:02:25 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 17 Jul 2020 01:51:26 GMT
ENV GOLANG_VERSION=1.14.6
# Fri, 17 Jul 2020 02:57:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '73fc9d781815d411928eccb92bf20d5b4264797be69410eac854babe44c94c09 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 17 Jul 2020 02:58:12 GMT
ENV GOPATH=/go
# Fri, 17 Jul 2020 02:58:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Jul 2020 02:59:06 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 17 Jul 2020 02:59:17 GMT
WORKDIR /go
# Fri, 17 Jul 2020 06:31:35 GMT
WORKDIR /src
# Fri, 17 Jul 2020 06:31:38 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 17 Jul 2020 06:31:39 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Fri, 17 Jul 2020 06:31:41 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Fri, 17 Jul 2020 06:31:42 GMT
WORKDIR /src/caddy/cmd/caddy
# Fri, 17 Jul 2020 06:33:01 GMT
RUN go get -d ./...
# Fri, 17 Jul 2020 06:33:06 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Fri, 17 Jul 2020 06:33:08 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:b4b72e716706d29f5d2351709c20bf737b94f876a5472a43ff1b6e203c65d27f`  
		Last Modified: Fri, 29 May 2020 21:51:30 GMT  
		Size: 2.6 MB (2603286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c276dc457bae632c9eadd1ac69c1a756a9a67e050b0350a475b19663722191cf`  
		Last Modified: Tue, 02 Jun 2020 05:21:23 GMT  
		Size: 282.8 KB (282778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f0819b703e39c232c6d0a8ac0f76d8f3c6856629db16fd6dd7b7ae69368281`  
		Last Modified: Tue, 02 Jun 2020 05:21:23 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25ebb22b58317c7858ae8af994cd3112c1fbea97cc7afb55adce8d18f9944e4`  
		Last Modified: Fri, 17 Jul 2020 06:13:08 GMT  
		Size: 128.6 MB (128623510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d433abc4dc297a87530213f798aa8f47f7d424d232a08e6ac1d29a2a140323cc`  
		Last Modified: Fri, 17 Jul 2020 06:12:25 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2380175eea4efe9fed5c27d515246917174c2a26e90472b0f003be9e87f31e`  
		Last Modified: Fri, 17 Jul 2020 06:33:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e30ddb2d12745d6245d848d9521271d43549c93a90b2f3e7d0604bec475735c`  
		Last Modified: Fri, 17 Jul 2020 06:33:35 GMT  
		Size: 7.9 MB (7928846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4925f56d53c2c18673aaeea837b60a3a6a1951caf78d34ad55363a4401660fe`  
		Last Modified: Fri, 17 Jul 2020 06:33:33 GMT  
		Size: 3.0 MB (3022759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f176349888c0f702bf42d452f55f66e0f66d49fec8781b620839a308788730b4`  
		Last Modified: Fri, 17 Jul 2020 06:34:57 GMT  
		Size: 184.2 MB (184238672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e191a4ff9c5c6ceb8798e721c1a18c1b9fefe507ddefd0f358d5966fbeddc8ef`  
		Last Modified: Fri, 17 Jul 2020 06:33:32 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e31fd005cc9631cb4d8b68f4ccdcbb8f3273d1c6d006558fa665864433f64b9`  
		Last Modified: Fri, 17 Jul 2020 06:33:33 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm variant v7

```console
$ docker pull caddy@sha256:0f07782410f2e87f4c0cb905502da9fbeeee0fa5c8b59b65aa5f22968050c841
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.3 MB (325311629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:238320344be4a4a482f3c046bf2b2cdd6d878326a4d7c2de5e320a2fb78ab2f3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:02:07 GMT
ADD file:e97bf0d217846312b19a9f7264604851aedd125c23b4d291eed4c69b880dce26 in / 
# Fri, 29 May 2020 21:02:08 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:10:58 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:11:00 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 17 Jul 2020 02:04:27 GMT
ENV GOLANG_VERSION=1.14.6
# Fri, 17 Jul 2020 03:11:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '73fc9d781815d411928eccb92bf20d5b4264797be69410eac854babe44c94c09 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 17 Jul 2020 03:11:28 GMT
ENV GOPATH=/go
# Fri, 17 Jul 2020 03:11:35 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Jul 2020 03:12:18 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 17 Jul 2020 03:12:31 GMT
WORKDIR /go
# Fri, 17 Jul 2020 06:47:30 GMT
WORKDIR /src
# Fri, 17 Jul 2020 06:47:33 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 17 Jul 2020 06:47:33 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Fri, 17 Jul 2020 06:47:36 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Fri, 17 Jul 2020 06:47:37 GMT
WORKDIR /src/caddy/cmd/caddy
# Fri, 17 Jul 2020 06:48:48 GMT
RUN go get -d ./...
# Fri, 17 Jul 2020 06:48:56 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Fri, 17 Jul 2020 06:48:57 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:52278dd8e57993669c5b72a9620e89bebdc098f2af2379caaa8945f7403f77a2`  
		Last Modified: Fri, 29 May 2020 21:02:38 GMT  
		Size: 2.4 MB (2406763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8512c25ce227edddad11326504a9bab47e83f8b61c090c9dc95882452984ac62`  
		Last Modified: Tue, 02 Jun 2020 03:51:20 GMT  
		Size: 281.9 KB (281892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87928ee7e6c788309b46621e351321410e4dde5374869ffa75f404b19e0e0c12`  
		Last Modified: Tue, 02 Jun 2020 03:51:20 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:386f5cddb797a50b33d215c68e6963c492ce158f4acb6321f10327d11cdf464c`  
		Last Modified: Fri, 17 Jul 2020 06:27:46 GMT  
		Size: 128.2 MB (128214215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d87c93a7694e8c03415e48886a81f26a4fd10467755ef509e37ab78593adfe`  
		Last Modified: Fri, 17 Jul 2020 06:27:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972c54955b6aa3316c0ff1cd09648a896cb6693602ab83c324d5c6837f9dc62c`  
		Last Modified: Fri, 17 Jul 2020 06:49:13 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d159a39289b70a909e7fd73e0e497cfd4eb983d918cce909ba18ef74df0e62d0`  
		Last Modified: Fri, 17 Jul 2020 06:49:13 GMT  
		Size: 7.1 MB (7144985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cca20950b907146caee82c433bca1179624f065f71ab28a8eb464be8a1f6225`  
		Last Modified: Fri, 17 Jul 2020 06:49:12 GMT  
		Size: 3.0 MB (3024202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e818a007e027c7573bd897dfe911528ca93ebc25c406e165820994e7d479f1d0`  
		Last Modified: Fri, 17 Jul 2020 06:49:59 GMT  
		Size: 184.2 MB (184238443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b3e0e2169e492b6bf7bef0b45af6ade994549689fc7fd916438830f7d2f704`  
		Last Modified: Fri, 17 Jul 2020 06:49:11 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9adec9e975b54335ac1a6dc75982c4a7d1fe45d5e781734fae0d4dc3108bdd7`  
		Last Modified: Fri, 17 Jul 2020 06:49:11 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; arm64 variant v8

```console
$ docker pull caddy@sha256:d9b385fc2cdf4dab3773895d129c95818687445f4475a67a8d334435fc124b40
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.7 MB (325665675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5e0552365aac8f035b32f4489273fee74e12eb50b1415582faf096e1b1f6ba`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:43:19 GMT
ADD file:7574aee4e37a85460ab889212d52912723a9b30dda1c060548f0deb4a05fc398 in / 
# Fri, 29 May 2020 21:43:20 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:57:21 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:58:08 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 17 Jul 2020 02:57:05 GMT
ENV GOLANG_VERSION=1.14.6
# Fri, 17 Jul 2020 03:04:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '73fc9d781815d411928eccb92bf20d5b4264797be69410eac854babe44c94c09 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 17 Jul 2020 03:04:35 GMT
ENV GOPATH=/go
# Fri, 17 Jul 2020 03:04:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Jul 2020 03:06:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 17 Jul 2020 03:06:23 GMT
WORKDIR /go
# Fri, 17 Jul 2020 03:58:20 GMT
WORKDIR /src
# Fri, 17 Jul 2020 03:59:13 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 17 Jul 2020 03:59:23 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Fri, 17 Jul 2020 04:00:14 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Fri, 17 Jul 2020 04:00:26 GMT
WORKDIR /src/caddy/cmd/caddy
# Fri, 17 Jul 2020 04:02:15 GMT
RUN go get -d ./...
# Fri, 17 Jul 2020 04:02:27 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Fri, 17 Jul 2020 04:02:42 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:b538f80385f9b48122e3da068c932a96ea5018afa3c7be79da00437414bd18cd`  
		Last Modified: Fri, 29 May 2020 21:43:57 GMT  
		Size: 2.7 MB (2707964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f711af9a0d350d42a1cb00f41feb32277e11189d70d84d76fdef5065f78c47`  
		Last Modified: Tue, 02 Jun 2020 02:29:25 GMT  
		Size: 283.0 KB (282997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f96fe45779b3ba9e9daededd02c233c5c76715ef1c5e88dd10c7acbea8414f`  
		Last Modified: Tue, 02 Jun 2020 02:29:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d59dbbba2831df4ad1849eb067f3f748541b207f42ca56d49a142e7fd95f8ea0`  
		Last Modified: Fri, 17 Jul 2020 03:36:05 GMT  
		Size: 126.9 MB (126913433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c21059ec65e133775c0fc8b223046bf6e2d766094029e1518d190fa9da1d0ee`  
		Last Modified: Fri, 17 Jul 2020 03:35:24 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ae716dd9416bf4c1d2b731527e6940b449f0590053887e451e6902cbcb86d2`  
		Last Modified: Fri, 17 Jul 2020 04:03:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6428ce7af4d06d38cc1ecbd978e44996d4020c88f8433609b9d22d57735ce3a`  
		Last Modified: Fri, 17 Jul 2020 04:03:07 GMT  
		Size: 8.5 MB (8499920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:671a0e3c8fa48586beafb4877bb9b41cab4dbb7a131bfc86469233d50d728d12`  
		Last Modified: Fri, 17 Jul 2020 04:03:05 GMT  
		Size: 3.0 MB (3022773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27df749c971337bab5044e3f90331c55a510db71c47c5fe2537fe2f00d4eb133`  
		Last Modified: Fri, 17 Jul 2020 04:03:45 GMT  
		Size: 184.2 MB (184237457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6350c2bdd79c91a5e63f9c3a0971718c84f1496fdfeb8ddbb9eff03fc74bebb2`  
		Last Modified: Fri, 17 Jul 2020 04:03:05 GMT  
		Size: 512.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab9b52f406680644fe33b63c216b5769077894847566e3fd0a448ba81ffc48d`  
		Last Modified: Fri, 17 Jul 2020 04:03:05 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; ppc64le

```console
$ docker pull caddy@sha256:6f0d7c9bb84c51ed939efb13e3bf6ca9446d49b9d6f85958f0fb138de6a5c564
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.9 MB (324933638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:833092067ee129e61a268dd93d22ceb73687f1de1cecd5e0df72bcda02dc5426`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:23:03 GMT
ADD file:8194808a812370fd2202d80d1667f851bd9eac4c560d69d347fe1964f54343de in / 
# Fri, 29 May 2020 21:23:06 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:29:37 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:29:54 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 17 Jul 2020 02:21:44 GMT
ENV GOLANG_VERSION=1.14.6
# Fri, 17 Jul 2020 02:24:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '73fc9d781815d411928eccb92bf20d5b4264797be69410eac854babe44c94c09 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 17 Jul 2020 02:24:14 GMT
ENV GOPATH=/go
# Fri, 17 Jul 2020 02:24:18 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Jul 2020 02:24:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 17 Jul 2020 02:24:36 GMT
WORKDIR /go
# Fri, 17 Jul 2020 03:12:38 GMT
WORKDIR /src
# Fri, 17 Jul 2020 03:12:56 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 17 Jul 2020 03:13:07 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Fri, 17 Jul 2020 03:13:21 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Fri, 17 Jul 2020 03:13:28 GMT
WORKDIR /src/caddy/cmd/caddy
# Fri, 17 Jul 2020 03:18:29 GMT
RUN go get -d ./...
# Fri, 17 Jul 2020 03:18:37 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Fri, 17 Jul 2020 03:18:43 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:5077f8601dceb5744d875d7740ebc203f674b108a0188f3a31e292b21a4bee64`  
		Last Modified: Fri, 29 May 2020 21:23:37 GMT  
		Size: 2.8 MB (2805199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d800b4e456ea05213bc7310b5d1b1706274430828a3c19a2fa8c6694733dc4`  
		Last Modified: Tue, 02 Jun 2020 01:48:21 GMT  
		Size: 285.0 KB (285034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a45a7c013c1132848fd122dfb4511c34ed884573ddfd7d8ad13d9a8a6157c42`  
		Last Modified: Tue, 02 Jun 2020 01:48:20 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:869ed739838c69d7e160dc1ff1fdd2300d17b52ee5d67aee493ca90d9b4fbd68`  
		Last Modified: Fri, 17 Jul 2020 02:45:38 GMT  
		Size: 125.7 MB (125656430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a61d3270248636b8a3f7205c3beff887ef7d4e2d403236b40d966e78b436f3`  
		Last Modified: Fri, 17 Jul 2020 02:43:02 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b42d4c77523f2d142783f55bea8336f93ff2cffd130887ca26938de15e3f7f`  
		Last Modified: Fri, 17 Jul 2020 03:19:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d23037bff9becbc5cea0824bae9147c00c87e29b5e83f2d3d3731d4542a3822`  
		Last Modified: Fri, 17 Jul 2020 03:19:09 GMT  
		Size: 8.9 MB (8920009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5927740889cdf47f4a17ea13d4bb5a9f5afca616c3c80b149e904f384b88bc64`  
		Last Modified: Fri, 17 Jul 2020 03:19:07 GMT  
		Size: 3.0 MB (3021040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa038742c660b74c276241553dd0dad4ad3ac9e8ad93d193a4c69258f93dff42`  
		Last Modified: Fri, 17 Jul 2020 03:19:34 GMT  
		Size: 184.2 MB (184244796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8514849ad61d3a9e0d21db033cc533db85e018c56ff97450ab8c55cfb2edca7e`  
		Last Modified: Fri, 17 Jul 2020 03:19:06 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75180876e9c63f9f97d6b4c520adaf9fe6fbfb5b935515aec347dbba6d8aa0c0`  
		Last Modified: Fri, 17 Jul 2020 03:19:06 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `caddy:builder` - linux; s390x

```console
$ docker pull caddy@sha256:6330b0180c606a640045d73f471239638e0082e1ac3de2ce2e799608b1403cff
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.7 MB (330732719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2744f7b60057c0c75e28371bfa6b50008bd9abfe4ce40e894258ec0fe5dfa00`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:41:39 GMT
ADD file:9799ce3b2f782a28e10b1846cd9b3db827fa99c9bc601feb268456195856814e in / 
# Fri, 29 May 2020 21:41:39 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2020 01:53:15 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 02 Jun 2020 01:53:16 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 17 Jul 2020 02:42:46 GMT
ENV GOLANG_VERSION=1.14.6
# Fri, 17 Jul 2020 02:44:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo '73fc9d781815d411928eccb92bf20d5b4264797be69410eac854babe44c94c09 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Fri, 17 Jul 2020 02:44:13 GMT
ENV GOPATH=/go
# Fri, 17 Jul 2020 02:44:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Jul 2020 02:44:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Fri, 17 Jul 2020 02:44:14 GMT
WORKDIR /go
# Fri, 17 Jul 2020 03:09:23 GMT
WORKDIR /src
# Fri, 17 Jul 2020 03:09:26 GMT
RUN apk add --no-cache     git     ca-certificates
# Fri, 17 Jul 2020 03:09:27 GMT
ENV CADDY_SOURCE_VERSION=v2.1.1
# Fri, 17 Jul 2020 03:09:29 GMT
RUN git clone -b $CADDY_SOURCE_VERSION https://github.com/caddyserver/caddy.git --single-branch
# Fri, 17 Jul 2020 03:09:30 GMT
WORKDIR /src/caddy/cmd/caddy
# Fri, 17 Jul 2020 03:10:20 GMT
RUN go get -d ./...
# Fri, 17 Jul 2020 03:10:41 GMT
COPY file:ed649bfc3baea8b334bfe88e6442632ecdc59b7c07d01b02a6c4558e5d77f98a in /usr/bin/caddy-builder 
# Fri, 17 Jul 2020 03:10:42 GMT
WORKDIR /src/custom-caddy/cmd/caddy
```

-	Layers:
	-	`sha256:8fb3d41b2e9a59630b51745f257cd2561f96bcd15cf309fcc20120d5fcee8c5b`  
		Last Modified: Fri, 29 May 2020 21:42:03 GMT  
		Size: 2.6 MB (2566189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2094092570892a8483a3fc940b327cccddf0cb7affb2a628ef4c98e40b4830bd`  
		Last Modified: Tue, 02 Jun 2020 02:01:04 GMT  
		Size: 283.1 KB (283144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b64a1c2f9ba0751e3e55cf33ddc6f0fd325bce1e6d64ef921f6258c5115b3c0`  
		Last Modified: Tue, 02 Jun 2020 02:01:04 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561add13be46fdce5a695d1ca8906ad50a90e3d3d25d47e1ad2c8478537bc445`  
		Last Modified: Fri, 17 Jul 2020 02:51:38 GMT  
		Size: 132.3 MB (132268907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f72d70911ac3c6bbdf16aa3d58a6bbe08cf171406e75d7dbf84c7ffd219073`  
		Last Modified: Fri, 17 Jul 2020 02:51:52 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38e21bb7fac2484df2339b1be77584264518b7a0dcb878869e6fade02cd7a2e`  
		Last Modified: Fri, 17 Jul 2020 03:11:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a5388655ece15f0d53ad7c41a2cdde6c25eab31b939efbe1eb3aa76c0279b3`  
		Last Modified: Fri, 17 Jul 2020 03:11:07 GMT  
		Size: 8.4 MB (8352234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4c55d0a142dc8b432c7f402cedd62737abb5d83f72caf89a1b0bed0066c6be`  
		Last Modified: Fri, 17 Jul 2020 03:11:11 GMT  
		Size: 3.0 MB (3024180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a5905cbf69b78060dd069e31cdabd5ee3a08eefaa57bc455415b85929755ac`  
		Last Modified: Fri, 17 Jul 2020 03:11:23 GMT  
		Size: 184.2 MB (184236938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af024d101834697f989a8213e8472351a541b76397f2be2fd6cdf79bef5292a8`  
		Last Modified: Fri, 17 Jul 2020 03:11:36 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7dbf6babd157dfc3f807bef9a82ac255c5c1c471919c8578aa0a4626d5f834`  
		Last Modified: Fri, 17 Jul 2020 03:11:36 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
