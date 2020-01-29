## `golang:1-alpine`

```console
$ docker pull golang@sha256:7e8c9c559ca6cf6535f501ca5eec46cae69489b5b8ef9cdec5abcaa5b09e707b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `golang:1-alpine` - linux; amd64

```console
$ docker pull golang@sha256:9817fae0190681da743ae2f5f77a85bf19b2e759d655bc427328e075b8d64dcc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129979252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87eefb76f0a85935d392182a0cb271178ee363516bdb3ca281a67c3b58ec491d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 02:06:05 GMT
RUN apk add --no-cache 		ca-certificates
# Sat, 18 Jan 2020 02:06:05 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 28 Jan 2020 21:20:19 GMT
ENV GOLANG_VERSION=1.13.7
# Tue, 28 Jan 2020 21:22:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo 'e4ad42cc5f5c19521fbbbde3680995f2546110b5c6aa2b48c3754ff7af9b41f4 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Tue, 28 Jan 2020 21:22:34 GMT
ENV GOPATH=/go
# Tue, 28 Jan 2020 21:22:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2020 21:22:35 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 28 Jan 2020 21:22:35 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb0d8da1b304e1b4f86e0a2fb11185850170e41986ce261dc30ac043c6a4e55`  
		Last Modified: Sat, 18 Jan 2020 02:17:12 GMT  
		Size: 301.3 KB (301262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d909eff282003e2d64af08633f4ae58f8cab4efc0a83b86579b4bbcb0ac90956`  
		Last Modified: Sat, 18 Jan 2020 02:17:12 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e7c84be0a12a0e5b3a305d8a08a7f456158c93a0b395c0d7a04b5029b42d9e`  
		Last Modified: Tue, 28 Jan 2020 21:32:14 GMT  
		Size: 126.9 MB (126874752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0c202c45dfb5a9f0304c67318677890c518b01a12815b925d5349f31df0945`  
		Last Modified: Tue, 28 Jan 2020 21:31:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:15e94bd381a7642b2d538ab8172345f37cd0b8bb1c0a59a0666eb83844b81916
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125681779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2116fe576916f815545efce5cf1fdca82bd67d0b0d64024bad3ce1be672f96b3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:53:16 GMT
ADD file:a1906f14a4e217a498b550f86a3d17c9012c02a6df0668043b63848c8fa44b9b in / 
# Sat, 18 Jan 2020 01:53:17 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 06:25:47 GMT
RUN apk add --no-cache 		ca-certificates
# Sat, 18 Jan 2020 06:26:01 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 28 Jan 2020 21:49:39 GMT
ENV GOLANG_VERSION=1.13.7
# Tue, 28 Jan 2020 21:52:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo 'e4ad42cc5f5c19521fbbbde3680995f2546110b5c6aa2b48c3754ff7af9b41f4 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Tue, 28 Jan 2020 21:52:52 GMT
ENV GOPATH=/go
# Tue, 28 Jan 2020 21:52:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2020 21:52:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 28 Jan 2020 21:52:55 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:832e07764099264ef96e50a1e5e41c52d6b0809bd054e29508a6878aa59d156d`  
		Last Modified: Sat, 18 Jan 2020 01:53:52 GMT  
		Size: 2.6 MB (2617562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d2b137a297685be92f7479a03dea76067a2661aad0f67c91123273b54a624ec`  
		Last Modified: Sat, 18 Jan 2020 06:37:07 GMT  
		Size: 301.6 KB (301631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439690e0c083aac08ba3afdf74ba79b8f50b530aed84c1d194e232c8ee4713a1`  
		Last Modified: Sat, 18 Jan 2020 06:37:07 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:896dfa666eecc83a89bb563b078532715df9704c4e18d4157c81d8c4fab69368`  
		Last Modified: Tue, 28 Jan 2020 22:03:32 GMT  
		Size: 122.8 MB (122762275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d6d3e79c0c45a88ed9a754c3bb9e7739d3b283cd9509233fa67d59b17db178`  
		Last Modified: Tue, 28 Jan 2020 22:02:59 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:07e0051866aa6cd44765d37af613a9efac3666956a5da3d092735ee9d4956514
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.1 MB (125115421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56d8850264881dd79fe6f115709a8e6bffdc5aa05251a3fa516ae99e5ca6c653`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 18 Jan 2020 02:03:19 GMT
ADD file:4c815f4461ff3b8d481f43d84eb2548cb1adbb3015d370cab86dd7f4d3d94279 in / 
# Sat, 18 Jan 2020 02:03:22 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 03:05:43 GMT
RUN apk add --no-cache 		ca-certificates
# Sat, 18 Jan 2020 03:05:47 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 28 Jan 2020 21:59:13 GMT
ENV GOLANG_VERSION=1.13.7
# Tue, 28 Jan 2020 22:01:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo 'e4ad42cc5f5c19521fbbbde3680995f2546110b5c6aa2b48c3754ff7af9b41f4 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Tue, 28 Jan 2020 22:01:52 GMT
ENV GOPATH=/go
# Tue, 28 Jan 2020 22:01:53 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2020 22:01:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 28 Jan 2020 22:01:56 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3a2c5e3c37b2e3d749405512ef3793aa45a2f5c11615d9e9efa80179262cdf27`  
		Last Modified: Sat, 18 Jan 2020 02:04:05 GMT  
		Size: 2.4 MB (2419554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67cc1a5632a818a23b346143b68a5f38c687431e4c6752c1c065fd45e4eb4cae`  
		Last Modified: Sat, 18 Jan 2020 03:15:43 GMT  
		Size: 300.6 KB (300566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321c622e107dd32aa9f0a955846018aa4ff6d211da03fb554cb91f1166eca153`  
		Last Modified: Sat, 18 Jan 2020 03:15:43 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c2e7e4e00c18dba2c994b78425ba017044971061923eec36c6811f40066b1a`  
		Last Modified: Tue, 28 Jan 2020 22:13:36 GMT  
		Size: 122.4 MB (122394992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84410b566d060dadeecfcd17a9eeefd471904fe73cd5fcc5236f45efe5334031`  
		Last Modified: Tue, 28 Jan 2020 22:12:55 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:0779517a1186ea2bfd892af9aebb2b5e635bd7c00831e806523c9fb77f51e9cc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124244433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ece1d5d65b784ba5ada6cff836c8f7bb8611a69e6838140f3570b069edb08f5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:39:43 GMT
ADD file:4109fa86dd80850e84c689ff9e6a3243e30ab1bbcc00c765969b3011bfbb43e1 in / 
# Sat, 18 Jan 2020 01:39:43 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 06:10:29 GMT
RUN apk add --no-cache 		ca-certificates
# Sat, 18 Jan 2020 06:10:36 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 28 Jan 2020 21:41:22 GMT
ENV GOLANG_VERSION=1.13.7
# Tue, 28 Jan 2020 21:43:19 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo 'e4ad42cc5f5c19521fbbbde3680995f2546110b5c6aa2b48c3754ff7af9b41f4 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Tue, 28 Jan 2020 21:43:22 GMT
ENV GOPATH=/go
# Tue, 28 Jan 2020 21:43:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2020 21:43:24 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 28 Jan 2020 21:43:25 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8fa90b21c985a6fcfff966bdfbde81cdd088de0aa8af38110057f6ac408f4408`  
		Last Modified: Sat, 18 Jan 2020 01:40:23 GMT  
		Size: 2.7 MB (2723075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3b0fa9a238a4fa3f590c80e14c5732f811f7a17aa0b8102cea7e3a9d250fcd`  
		Last Modified: Sat, 18 Jan 2020 06:20:51 GMT  
		Size: 301.8 KB (301775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:583d88f014275e361b79e5a5ccf10b177aafe63e5d44ccd5d3911ca9b924efac`  
		Last Modified: Sat, 18 Jan 2020 06:20:51 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802e4b917718c95809fa84359b28d2c6812f7a960dd880fe80a4c7ebdb280a4f`  
		Last Modified: Tue, 28 Jan 2020 21:53:50 GMT  
		Size: 121.2 MB (121219273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8186cbf5ad8e1034a787322d0f075e89042d6398e1b1026327086095523f2d`  
		Last Modified: Tue, 28 Jan 2020 21:53:22 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-alpine` - linux; 386

```console
$ docker pull golang@sha256:9202dba0118f1eb416116f3845f1f25bbf926a57ee0c59b7ffc9fbc638026117
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.7 MB (129665781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:298654712cdc29b7267d268eaa5ea049dd3ce752070e7d3e6433441a9224d2b9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:38:44 GMT
ADD file:381b617b92fe699ad4ef4f30e0d9599f89e43e252883348c420ebe2a0cccbd63 in / 
# Sat, 18 Jan 2020 01:38:45 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 07:02:55 GMT
RUN apk add --no-cache 		ca-certificates
# Sat, 18 Jan 2020 07:02:56 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 28 Jan 2020 21:39:15 GMT
ENV GOLANG_VERSION=1.13.7
# Tue, 28 Jan 2020 21:42:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo 'e4ad42cc5f5c19521fbbbde3680995f2546110b5c6aa2b48c3754ff7af9b41f4 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Tue, 28 Jan 2020 21:42:01 GMT
ENV GOPATH=/go
# Tue, 28 Jan 2020 21:42:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2020 21:42:02 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 28 Jan 2020 21:42:02 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f024b1263dc58db07a458b73ae1a2dca02ca55bef1ccd1fa3fd50656551fadf2`  
		Last Modified: Sat, 18 Jan 2020 01:39:18 GMT  
		Size: 2.8 MB (2806560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51d08eae3dcf47cd450c87c9ea787c8293e63405c12eb6ab24dbc68d5f1c126`  
		Last Modified: Sat, 18 Jan 2020 07:11:57 GMT  
		Size: 301.9 KB (301918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93286c43ae8d1560f8d4f4591d4ac47b8532570a50267d7f0df83626ad9d77b7`  
		Last Modified: Sat, 18 Jan 2020 07:11:56 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd7e7f297de156475032c56c51904e5d5d25a3eea238fef14820c24645cbb0a`  
		Last Modified: Tue, 28 Jan 2020 21:52:47 GMT  
		Size: 126.6 MB (126557025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34912ef29244fc054137e09463742b477e6935c71b4a43f12a332c692fa806ee`  
		Last Modified: Tue, 28 Jan 2020 21:52:20 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:d689c8216da034556203b8dbb6bf0673f80024f4a9e3b1267af3c9a4f7fb960b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123107017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aca48a49e6cbee68e6425e198f7e9302d8b425904aaf350de794bcbeed5d766a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 18 Jan 2020 02:20:41 GMT
ADD file:32ddb3d5255071cca51573ceee2464dd5a87c8d1cce514ae965b6e824d9ef24b in / 
# Sat, 18 Jan 2020 02:20:45 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 04:46:12 GMT
RUN apk add --no-cache 		ca-certificates
# Sat, 18 Jan 2020 04:46:18 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 28 Jan 2020 21:18:26 GMT
ENV GOLANG_VERSION=1.13.7
# Tue, 28 Jan 2020 21:20:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo 'e4ad42cc5f5c19521fbbbde3680995f2546110b5c6aa2b48c3754ff7af9b41f4 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Tue, 28 Jan 2020 21:20:31 GMT
ENV GOPATH=/go
# Tue, 28 Jan 2020 21:20:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2020 21:20:37 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 28 Jan 2020 21:20:40 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cd95c8a93e39dcaa0634a65d5b86a88bcd5c3092adb1f96504a7030faa165123`  
		Last Modified: Sat, 18 Jan 2020 02:21:25 GMT  
		Size: 2.8 MB (2822125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75713e636f3d39d3f2654c04e99be412afb204d9a236849bd298a759cbf05081`  
		Last Modified: Sat, 18 Jan 2020 04:54:33 GMT  
		Size: 304.0 KB (303987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe2d35b38ecf395171885c1576a18a065e4580f2a1e83771da3f4de412af0712`  
		Last Modified: Sat, 18 Jan 2020 04:54:33 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f04ce87d6b98729f40474c01b962e436dd8bd4d47db4c4e5071f64ffa0a15a8`  
		Last Modified: Tue, 28 Jan 2020 21:32:01 GMT  
		Size: 120.0 MB (119980595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68dd017643b4f890a476c651249c770035b37cc57d3f6349bd69fd28ab4ccbdc`  
		Last Modified: Tue, 28 Jan 2020 21:31:20 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-alpine` - linux; s390x

```console
$ docker pull golang@sha256:a0629f55953d6453043d465307acd6a1eaa7e724aba5246f426e2f3fea69d5b7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.7 MB (129728232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f109e154bac5476d05e1851d56796db85a1acaeb6e56328d08e0228c9cc17a7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 18 Jan 2020 01:41:33 GMT
ADD file:a6f8b7d4ba199527053ef1ac710b5e318135cb6903cb9ad6fae4fe42e6ad0bf7 in / 
# Sat, 18 Jan 2020 01:41:33 GMT
CMD ["/bin/sh"]
# Sat, 18 Jan 2020 01:42:23 GMT
RUN apk add --no-cache 		ca-certificates
# Sat, 18 Jan 2020 01:42:24 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 28 Jan 2020 21:44:18 GMT
ENV GOLANG_VERSION=1.13.7
# Tue, 28 Jan 2020 21:45:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bash 		gcc 		musl-dev 		openssl 		go 	; 	export 		GOROOT_BOOTSTRAP="$(go env GOROOT)" 		GOOS="$(go env GOOS)" 		GOARCH="$(go env GOARCH)" 		GOHOSTOS="$(go env GOHOSTOS)" 		GOHOSTARCH="$(go env GOHOSTARCH)" 	; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		armhf) export GOARM='6' ;; 		armv7) export GOARM='7' ;; 		x86) export GO386='387' ;; 	esac; 		wget -O go.tgz "https://golang.org/dl/go$GOLANG_VERSION.src.tar.gz"; 	echo 'e4ad42cc5f5c19521fbbbde3680995f2546110b5c6aa2b48c3754ff7af9b41f4 *go.tgz' | sha256sum -c -; 	tar -C /usr/local -xzf go.tgz; 	rm go.tgz; 		cd /usr/local/go/src; 	./make.bash; 		rm -rf 		/usr/local/go/pkg/bootstrap 		/usr/local/go/pkg/obj 	; 	apk del .build-deps; 		export PATH="/usr/local/go/bin:$PATH"; 	go version
# Tue, 28 Jan 2020 21:45:29 GMT
ENV GOPATH=/go
# Tue, 28 Jan 2020 21:45:29 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2020 21:45:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
# Tue, 28 Jan 2020 21:45:30 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:176bad61a3a435da03ec603d2bd8f7a69286d92f21f447b17f21f0bc4e085bde`  
		Last Modified: Sat, 18 Jan 2020 01:41:59 GMT  
		Size: 2.6 MB (2582031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5098d3328eb232d7f1890bea7d184bb878fdd3fd6f662f587ed0a70612d5587`  
		Last Modified: Sat, 18 Jan 2020 01:47:22 GMT  
		Size: 301.8 KB (301795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95cfc0bf895b01244b27aba1473ab54b274b1d43e1aacc52256be747e0835a38`  
		Last Modified: Sat, 18 Jan 2020 01:47:22 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10416da369ddc9c21001b9dcebc5c72c46ea34d7b6f63383eadf52ad721a4b47`  
		Last Modified: Tue, 28 Jan 2020 21:52:10 GMT  
		Size: 126.8 MB (126844094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e176f9abe0f87d87acb72f16c7ef2cedd1dfacfec53973e9dbe8e9bb93d5b90`  
		Last Modified: Tue, 28 Jan 2020 21:52:09 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
